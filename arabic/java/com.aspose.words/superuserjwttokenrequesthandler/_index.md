---
title: "SuperUserJwtTokenRequestHandler"
linktitle: "SuperUserJwtTokenRequestHandler"
second_title: "Aspose.Words لـ Java"
description: "معالج طلب رمز JWT مع التخزين المؤقت والتحقق المحلي وقاطع الدائرة في Java."
type: docs
weight: 648
url: /ar/java/com.aspose.words/superuserjwttokenrequesthandler/
---

**Inheritance:**
java.lang.Object
```
public class SuperUserJwtTokenRequestHandler
```

معالج طلب رمز JWT مع التخزين المؤقت، والتحقق المحلي، وقاطع الدائرة. يتم تخزين الرموز مؤقتًا لمدة تصل إلى 7 أيام مع تحديث قبل 6 ساعات من انتهاء الصلاحية.
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [SuperUserJwtTokenRequestHandler()](#SuperUserJwtTokenRequestHandler) | منشئ عام. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [beforeSend(HttpURLConnection request, OutputStream streamToSend)](#beforeSend-java.net.HttpURLConnection-java.io.OutputStream) | أضف رأس التفويض قبل إرسال الطلب. |
| [getCachedToken()](#getCachedToken) | يحصل على الرمز المميز المخزن مؤقتًا حاليًا لأغراض الاختبار. |
| [getTokenExpiration()](#getTokenExpiration) | يحصل على تاريخ انتهاء صلاحية الرمز المميز ككائن Date لأغراض الاختبار. |
| [getTokenExpirationMillis()](#getTokenExpirationMillis) | يحصل على وقت انتهاء صلاحية الرمز المميز لأغراض الاختبار. |
| [processResponse(HttpURLConnection response, String resultString, String errorString)](#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String) | معالجة الاستجابة، مع التعامل مع الخطأ 401 غير المصرح به عن طريق تجديد الرمز المميز. |
| [processUrl(String url)](#processUrl-java.lang.String) | معالجة عنوان URL (يتأكد من توفر الرمز المميز). |
| [resetForTesting()](#resetForTesting) | إعادة ضبط جميع حالات الرمز المميز المخزنة مؤقتًا لأغراض الاختبار. |
### SuperUserJwtTokenRequestHandler() {#SuperUserJwtTokenRequestHandler}
```
public SuperUserJwtTokenRequestHandler()
```


منشئ عام.

### beforeSend(HttpURLConnection request, OutputStream streamToSend) {#beforeSend-java.net.HttpURLConnection-java.io.OutputStream}
```
public void beforeSend(HttpURLConnection request, OutputStream streamToSend)
```


أضف رأس التفويض قبل إرسال الطلب.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| طلب | java.net.HttpURLConnection | الاتصال HTTP |
| streamToSend | java.io.OutputStream | دفق الإخراج (غير مستخدم) |

### getCachedToken() {#getCachedToken}
```
public static String getCachedToken()
```


يحصل على الرمز المميز المخزن مؤقتًا حاليًا لأغراض الاختبار.

**Returns:**
java.lang.String - الرمز المميز JWT المخزن مؤقتًا أو null
### getTokenExpiration() {#getTokenExpiration}
```
public static Date getTokenExpiration()
```


يحصل على تاريخ انتهاء صلاحية الرمز المميز ككائن Date لأغراض الاختبار.

**Returns:**
java.util.Date - تاريخ الانتهاء أو null إذا لا يوجد رمز
### getTokenExpirationMillis() {#getTokenExpirationMillis}
```
public static long getTokenExpirationMillis()
```


يحصل على وقت انتهاء صلاحية الرمز المميز لأغراض الاختبار.

**Returns:**
long - وقت الانتهاء بالمللي ثانية منذ epoch
### processResponse(HttpURLConnection response, String resultString, String errorString) {#processResponse-java.net.HttpURLConnection-java.lang.String-java.lang.String}
```
public void processResponse(HttpURLConnection response, String resultString, String errorString)
```


معالجة الاستجابة، مع التعامل مع الخطأ 401 غير المصرح به عن طريق تجديد الرمز المميز.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| استجابة | java.net.HttpURLConnection | استجابة HTTP |
| resultString | java.lang.String | محتوى الاستجابة |
| errorString | java.lang.String | رسالة الخطأ إن وجدت |

### processUrl(String url) {#processUrl-java.lang.String}
```
public String processUrl(String url)
```


معالجة عنوان URL (يتأكد من توفر الرمز المميز).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| url | java.lang.String | عنوان URL للمعالجة |

**Returns:**
java.lang.String - عنوان URL دون تعديل
### resetForTesting() {#resetForTesting}
```
public static void resetForTesting()
```


إعادة ضبط جميع حالات الرمز المميز المخزنة مؤقتًا لأغراض الاختبار.

