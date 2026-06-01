Növbəti: [Massivin Elanı](Declaring-an-Array.md), Yuxarı:
[Massivlər](Arrays.md)  
[Mündəricat](index.md#SEC_Contents "Mündəricat")

------------------------------------------------------------------------

### 16.1 Massiv Elementlərinə Giriş

Əgər `a` dəyişəni bir massivdirsə, `a` massivinin `n`-ci elementi
`a[n]` şəklində göstərilir. Bu ifadədən həm elementin dəyərini oxumaq,
həm də ona dəyər təyin etmək üçün istifadə edə bilərsiniz:

```C
x = a[5];
a[6] = 1;
```

`a` dəyişəni bir lvalue olduğu üçün `a[n]` də lvalue hesab olunur.

Massivdə ən kiçik etibarlı indeks 0-dır, *1 deyil*, və ən böyük etibarlı
indeks elementlərin sayından bir vahid azdır.

C dili massiv indekslərinin sərhədlər daxilində olub-olmadığını yoxlamır.
Buna görə də kod diapazondan kənar indeks istifadə edərsə, massivdən
kənardakı yaddaşa müraciət edəcəkdir.

**Xəbərdarlıq:** C dilində yalnız etibarlı indeks dəyərlərindən istifadə
etmək proqramçının məsuliyyətidir.

C dilində massiv indekslənməsi ilkin (primitive) əməliyyat deyil; o,
göstərici (pointer) arifmetikası və dereferens etmə əsasında təyin olunur.
İndi artıq `a[i]` ifadəsinin *nə etdiyini* bildiyimiz üçün, onun bunu
*nə cür etdiyini* soruşa bilərik.

C dilində `x[y]` ifadəsi `*(x+y)` üçün qısaldılmış yazılışdır. Buna görə
də `a[i]` əslində `*(a+i)` deməkdir. Bax:
[Göstəricilər və Massivlər](Pointers-and-Arrays.md).

Massiv tipli bir ifadə (məsələn, `a`) daha böyük bir C ifadəsinin tərkibində
işləndikdə, avtomatik olaraq həmin massivin sıfırıncı elementinə göstəriciyə
(pointer) çevrilir. Məsələn, ifadə daxilindəki `a`, `&a[0]` ilə ekvivalentdir.
Beləliklə, `*(a+i)` ifadəsi əslində `*(&a[0]+i)` kimi hesablanır.

İndi bu ifadənin necə istənilən massiv elementini verdiyini təhlil edə bilərik.
Əvvəlcə `a` massivinin 0-cı elementinə göstərici yaradır, sonra onu `i`
qədər irəli aparır və sonda həmin göstəricini dereferens edir.

Bu ifadəni yazmağın başqa bir ekvivalent üsulu da `(&a[0])[i]` şəklidir.

------------------------------------------------------------------------

Növbəti: [Massivin Elanı](Declaring-an-Array.md), Yuxarı:
[Massivlər](Arrays.md)  
[Mündəricat](index.md#SEC_Contents "Mündəricat")
