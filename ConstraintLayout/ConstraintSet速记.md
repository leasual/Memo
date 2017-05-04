### 0x81 ConstraintLayout
Google��֮ǰ��GoogleIO�����������ȫ�µ�Android�����������ConstraintLayout��������Լ�����֣�����ظ����е�����iOS�Ĳ���Լ������������Ҳ���Ը��õ��ڲ��ֱ༭�����������ק���в����ˡ�

### 0x82 ConstraintSet
Լ�����ִ�����support���У������ݴ󲿷ְ汾�����ڲ��ֵ������͸��ġ�GoogleΪ�����ṩ��һ��API���������Ǿ�������ConstraintSet����ࡣ

### 0x83 ConstraintSetʹ��
1. ��ȡ��������
```Java
ConstraintSet applyConstraintSet = new ConstraintSet();
ConstraintLayout clContact = (ConstraintLayout) rootView.findViewById(R.id.cl_contact);
applyConstraintSet.clone(clContact);
```
�������Ǳ���Ѿ�����õĲ�����ȡ��Լ�����Լ���

2. ��������
```Java
applyConstraintSet.setMargin(R.id.btn_contact1, ConstraintSet.START, 0);
applyConstraintSet.setMargin(R.id.btn_contact1, ConstraintSet.TOP, 0);
applyConstraintSet.setMargin(R.id.btn_contact1, ConstraintSet.END, 0);
applyConstraintSet.setMargin(R.id.btn_contact1, ConstraintSet.BOTTOM, 0);
```
�÷�������3��������һ��������View��id��һ���߽�������һ����ֵ��

3. ���ÿ��
```Java
applyConstraintSet.constrainWidth(R.id.btn_contact2, 500);
applyConstraintSet.constrainHeight(R.id.btn_contact1, ConstraintSet.WRAP_CONTENT);
```
�÷�������2��������������View��id��Ҫ���õ���ֵ��

4. ���þ���
```Java
applyConstraintSet.centerHorizontally(R.id.btn_contact1, R.id.cl_contact);
applyConstraintSet.centerVertically(R.id.btn_contact1, R.id.cl_contact);
```
�����÷�����`R.id.btn_contact1`��`R.id.cl_contact`�к������С�

5. ������ϵ
```Java
applyConstraintSet.connect(R.id.btn_contact1, ConstraintSet.START, R.id.cl_contact, ConstraintSet.START, 0);
applyConstraintSet.connect(R.id.btn_contact1, ConstraintSet.END, R.id.cl_contact, ConstraintSet.END, 0);
```
��������5����������һ���͵�������Ҫ������id���˴���������View�͸�View���ڶ����͵��ĸ��ǹ����߽磬��5�����趨��ֵ��
������ʾ��`R.id.btn_contact1`�Ŀ��ռ�������֡�

6. chaining
```Java
chainConstraintSet.connect(R.id.btn_contact1, ConstraintSet.START, R.id.cl_contact,
        ConstraintSet.START, 0);
chainConstraintSet.connect(R.id.btn_contact4, ConstraintSet.ER.id.cl_contact,
        ConstraintSet.END, 0);
chainConstraintSet.connect(R.id.btn_contact2, ConstraintSet.START,
        R.id.btn_contact1, ConstraintSet.END, 0);
chainConstraintSet.connect(R.id.btn_contact1, ConstraintSet.ER.id.btn_contact2,
        ConstraintSet.START, 0);
chainConstraintSet.connect(R.id.btn_contact3, ConstraintSet.START,
        R.id.btn_contact2, ConstraintSet.END, 0);
chainConstraintSet.connect(R.id.btn_contact2, ConstraintSet.ER.id.btn_contact3,
        ConstraintSet.START, 0);
chainConstraintSet.connect(R.id.btn_contact4, ConstraintSet.START,
        R.id.btn_contact3, ConstraintSet.END, 0);
chainConstraintSet.connect(R.id.btn_contact3, ConstraintSet.ER.id.btn_contact4,
        ConstraintSet.START, 

chainConstraintSet.createHorizontalChain(R.id.btn_contact_1, ConstraintSet.LEFT,
        R.id.btn_contact4, ConstraintSet.RIGHT,
        new int[]{R.id.btn_contact1, R.id.btn_contact4}, null,
        ConstraintWidget.CHAIN_SPREAD);
```
ͬ���ǹ����߽磬����ʹ��create*Chain��������Chain�������ֱ�ָ��������ViewId��������Viewλ�á���β��ViewId����β��Viewλ�á�ChainԪ�����顢����ֵ���顢ChainMode��

7. �����Ӧ��
```Java
applyConstraintSet.clear(R.id.btn_contact1);
applyConstraintSet.applyTo(clContact);
```
��һ�������`R.id.btn_contact1`������Լ�����ԣ�ע��������Ҳ�ǡ�
�ڶ����ǽ��µ�Լ������Ӧ�õ�Լ�������ϡ�

����ContraintSet�ļ�ʹ�þ���ô�࡫