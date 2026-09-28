---
title: DigitalSignatureTimestampSettings
linktitle: DigitalSignatureTimestampSettings
second_title: Aspose.Words for Java
description: Contains settings of the digital signature timestamp in Java.
type: docs
weight: 153
url: /java/com.aspose.words/digitalsignaturetimestampsettings/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignatureTimestampSettings
```

Contains settings of the digital signature timestamp.

 **Examples:** 

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```
## Constructors

| Constructor | Description |
| --- | --- |
| [DigitalSignatureTimestampSettings()](#DigitalSignatureTimestampSettings) | Initializes a new instance of [DigitalSignatureTimestampSettings](../../com.aspose.words/digitalsignaturetimestampsettings/) class. |
| [DigitalSignatureTimestampSettings(String serverUrl, String userName, String password)](#DigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String) | Initializes a new instance of [DigitalSignatureTimestampSettings](../../com.aspose.words/digitalsignaturetimestampsettings/) class. |
| [DigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout)](#DigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-long) | Initializes a new instance of [DigitalSignatureTimestampSettings](../../com.aspose.words/digitalsignaturetimestampsettings/) class. |
## Methods

| Method | Description |
| --- | --- |
| [getPassword()](#getPassword) | Gets a string value representing timestamp server password. |
| [getServerUrl()](#getServerUrl) | Gets a string value representing timestamp server URL. |
| [getTimeout()](#getTimeout) | Gets a time-out value for accessing timestamp server. |
| [getUserName()](#getUserName) | Gets a string value representing timestamp server user name. |
| [setPassword(String value)](#setPassword-java.lang.String) | Sets a string value representing timestamp server password. |
| [setServerUrl(String value)](#setServerUrl-java.lang.String) | Sets a string value representing timestamp server URL. |
| [setTimeout(long value)](#setTimeout-long) | Sets a time-out value for accessing timestamp server. |
| [setUserName(String value)](#setUserName-java.lang.String) | Sets a string value representing timestamp server user name. |
### DigitalSignatureTimestampSettings() {#DigitalSignatureTimestampSettings}
```
public DigitalSignatureTimestampSettings()
```


Initializes a new instance of [DigitalSignatureTimestampSettings](../../com.aspose.words/digitalsignaturetimestampsettings/) class.

### DigitalSignatureTimestampSettings(String serverUrl, String userName, String password) {#DigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String}
```
public DigitalSignatureTimestampSettings(String serverUrl, String userName, String password)
```


Initializes a new instance of [DigitalSignatureTimestampSettings](../../com.aspose.words/digitalsignaturetimestampsettings/) class.

 **Examples:** 

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| serverUrl | java.lang.String | Timestamp server URL. |
| userName | java.lang.String | Timestamp server user name. |
| password | java.lang.String | Timestamp server password. |

### DigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout) {#DigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-long}
```
public DigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout)
```


Initializes a new instance of [DigitalSignatureTimestampSettings](../../com.aspose.words/digitalsignaturetimestampsettings/) class.

 **Examples:** 

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| serverUrl | java.lang.String | Timestamp server URL. |
| userName | java.lang.String | Timestamp server user name. |
| password | java.lang.String | Timestamp server password. |
| timeout | long | Time-out value for accessing timestamp server. |

### getPassword() {#getPassword}
```
public String getPassword()
```


Gets a string value representing timestamp server password. The default value is  null .

 **Remarks:** 

 **Examples:** 

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```

**Returns:**
java.lang.String - A string value representing timestamp server password.
### getServerUrl() {#getServerUrl}
```
public String getServerUrl()
```


Gets a string value representing timestamp server URL. The default value is  null .

 **Remarks:** 

If  null , then the digital signature will not be time-stamped.

 **Examples:** 

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```

**Returns:**
java.lang.String - A string value representing timestamp server URL.
### getTimeout() {#getTimeout}
```
public long getTimeout()
```


Gets a time-out value for accessing timestamp server. The default value is 100 seconds.

 **Examples:** 

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```

**Returns:**
long - A time-out value for accessing timestamp server.
### getUserName() {#getUserName}
```
public String getUserName()
```


Gets a string value representing timestamp server user name. The default value is  null .

 **Remarks:** 

 **Examples:** 

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```

**Returns:**
java.lang.String - A string value representing timestamp server user name.
### setPassword(String value) {#setPassword-java.lang.String}
```
public void setPassword(String value)
```


Sets a string value representing timestamp server password. The default value is  null .

 **Remarks:** 

 **Examples:** 

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A string value representing timestamp server password. |

### setServerUrl(String value) {#setServerUrl-java.lang.String}
```
public void setServerUrl(String value)
```


Sets a string value representing timestamp server URL. The default value is  null .

 **Remarks:** 

If  null , then the digital signature will not be time-stamped.

 **Examples:** 

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A string value representing timestamp server URL. |

### setTimeout(long value) {#setTimeout-long}
```
public void setTimeout(long value)
```


Sets a time-out value for accessing timestamp server. The default value is 100 seconds.

 **Examples:** 

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | long | A time-out value for accessing timestamp server. |

### setUserName(String value) {#setUserName-java.lang.String}
```
public void setUserName(String value)
```


Sets a string value representing timestamp server user name. The default value is  null .

 **Remarks:** 

 **Examples:** 

Shows how to sign a document with timestamping using DigitalSignatureUtil.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_T);
     signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
             "https://freetsa.org/tsr",
             "JohnDoe",
             "MyPassword"));
 }

 CertificateHolder cert = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.Timestamped.docx");

 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signedDoc.getDigitalSignatures().get(0).isValid());

 // Verify timestamp settings are applied.
 Assert.assertEquals("https://freetsa.org/tsr", signOptions.getTimestampSettings().getServerUrl());
 Assert.assertEquals("JohnDoe", signOptions.getTimestampSettings().getUserName());
 Assert.assertEquals("MyPassword", signOptions.getTimestampSettings().getPassword());
 Assert.assertEquals(100.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());

 // Test with custom timeout.
 signOptions.setTimestampSettings(new DigitalSignatureTimestampSettings(
         "https://freetsa.org/tsr",
         "JohnDoe",
         "MyPassword",
         Duration.ofMinutes(30)));

 Assert.assertEquals(1800.0d, signOptions.getTimestampSettings().getTimeout().getTotalSeconds());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A string value representing timestamp server user name. |

