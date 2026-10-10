---
title: "X509Certificate2Wrapper"
linktitle: "X509Certificate2Wrapper"
second_title: "Aspose.Words لـ Java"
description: "غلاف عام أُضيف في Java حول X509Certificate2 الداخلي لدينا في Java."
type: docs
weight: 739
url: /ar/java/com.aspose.words/x509certificate2wrapper/
---

**Inheritance:**
java.lang.Object
```
public class X509Certificate2Wrapper
```

غلاف عام أُضيف في Java حول X509Certificate2 الداخلي لدينا. تم الحاجة إليه لمحاكاة واجهة .Net بسلاسة وتبسيط كود المستخدم في Java. من الناحية المثالية يجب استخدام java.security.cert.X509Certificate بدلاً من ذلك، لكننا لم نتمكن بعد من الحصول على المفتاح الخاص من X509Certificate في Java - قد يتم إصلاح ذلك لاحقًا.
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [X509Certificate2Wrapper(String fileName, String password)](#X509Certificate2Wrapper-java.lang.String-java.lang.String) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getJavaCertificateInfo()](#getJavaCertificateInfo) | يُستخدم شهادة Java للحصول على معلومات شهادة عامة: notBefore، notAfter، إلخ. |
### X509Certificate2Wrapper(String fileName, String password) {#X509Certificate2Wrapper-java.lang.String-java.lang.String}
```
public X509Certificate2Wrapper(String fileName, String password)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String |  |
| كلمة مرور | java.lang.String |  |

### getJavaCertificateInfo() {#getJavaCertificateInfo}
```
public X509Certificate getJavaCertificateInfo()
```


يُستخدم شهادة Java للحصول على معلومات شهادة عامة: notBefore، notAfter، إلخ.

**Returns:**
java.security.cert.X509Certificate
