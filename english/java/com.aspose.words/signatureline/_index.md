---
title: SignatureLine
second_title: Aspose.Words for Java API Reference
description: Provides access to signature line properties.
type: docs
weight: 524
url: /java/com.aspose.words/signatureline/
---

**Inheritance:**
java.lang.Object
```
public class SignatureLine
```

Provides access to signature line properties.

To learn more, visit the **Work with Digital Signatures** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getSigner()](#getSigner--) | Gets suggested signer of the signature line. |
| [setSigner(String value)](#setSigner-java.lang.String-) | Sets suggested signer of the signature line. |
| [getSignerTitle()](#getSignerTitle--) | Gets suggested signer's title (for example, Manager). |
| [setSignerTitle(String value)](#setSignerTitle-java.lang.String-) | Sets suggested signer's title (for example, Manager). |
| [getEmail()](#getEmail--) | Gets suggested signer's e-mail address. |
| [setEmail(String value)](#setEmail-java.lang.String-) | Sets suggested signer's e-mail address. |
| [getDefaultInstructions()](#getDefaultInstructions--) | Gets a value indicating that default instructions is shown in the Sign dialog. |
| [setDefaultInstructions(boolean value)](#setDefaultInstructions-boolean-) | Sets a value indicating that default instructions is shown in the Sign dialog. |
| [getInstructions()](#getInstructions--) | Gets instructions to the signer that are displayed on signing the signature line. |
| [setInstructions(String value)](#setInstructions-java.lang.String-) | Sets instructions to the signer that are displayed on signing the signature line. |
| [getAllowComments()](#getAllowComments--) | Gets a value indicating that the signer can add comments in the Sign dialog. |
| [setAllowComments(boolean value)](#setAllowComments-boolean-) | Sets a value indicating that the signer can add comments in the Sign dialog. |
| [getShowDate()](#getShowDate--) | Gets a value indicating that sign date is shown in the signature line. |
| [setShowDate(boolean value)](#setShowDate-boolean-) | Sets a value indicating that sign date is shown in the signature line. |
| [getId()](#getId--) | Gets identifier for this signature line. |
| [setId(UUID value)](#setId-java.util.UUID-) | Sets identifier for this signature line. |
| [getProviderId()](#getProviderId--) | Gets signature provider identifier for this signature line. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID-) | Sets signature provider identifier for this signature line. |
| [isSigned()](#isSigned--) | Indicates that signature line is signed by digital signature. |
| [isValid()](#isValid--) | Indicates that signature line is signed by digital signature and this digital signature is valid. |
### getSigner() {#getSigner--}
```
public String getSigner()
```


Gets suggested signer of the signature line. Default value for this property is **empty string**.

**Returns:**
java.lang.String - Suggested signer of the signature line.
### setSigner(String value) {#setSigner-java.lang.String-}
```
public void setSigner(String value)
```


Sets suggested signer of the signature line. Default value for this property is **empty string**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Suggested signer of the signature line. |

### getSignerTitle() {#getSignerTitle--}
```
public String getSignerTitle()
```


Gets suggested signer's title (for example, Manager). Default value for this property is **empty string**.

**Returns:**
java.lang.String - Suggested signer's title (for example, Manager).
### setSignerTitle(String value) {#setSignerTitle-java.lang.String-}
```
public void setSignerTitle(String value)
```


Sets suggested signer's title (for example, Manager). Default value for this property is **empty string**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Suggested signer's title (for example, Manager). |

### getEmail() {#getEmail--}
```
public String getEmail()
```


Gets suggested signer's e-mail address. Default value for this property is **empty string**.

**Returns:**
java.lang.String - Suggested signer's e-mail address.
### setEmail(String value) {#setEmail-java.lang.String-}
```
public void setEmail(String value)
```


Sets suggested signer's e-mail address. Default value for this property is **empty string**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Suggested signer's e-mail address. |

### getDefaultInstructions() {#getDefaultInstructions--}
```
public boolean getDefaultInstructions()
```


Gets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is **true**.

**Returns:**
boolean - A value indicating that default instructions is shown in the Sign dialog.
### setDefaultInstructions(boolean value) {#setDefaultInstructions-boolean-}
```
public void setDefaultInstructions(boolean value)
```


Sets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is **true**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating that default instructions is shown in the Sign dialog. |

### getInstructions() {#getInstructions--}
```
public String getInstructions()
```


Gets instructions to the signer that are displayed on signing the signature line. This property is ignored if [getDefaultInstructions()](../../com.aspose.words/signatureline\#getDefaultInstructions--) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline\#setDefaultInstructions-boolean-) is set. Default value for this property is **empty string**.

**Returns:**
java.lang.String - Instructions to the signer that are displayed on signing the signature line.
### setInstructions(String value) {#setInstructions-java.lang.String-}
```
public void setInstructions(String value)
```


Sets instructions to the signer that are displayed on signing the signature line. This property is ignored if [getDefaultInstructions()](../../com.aspose.words/signatureline\#getDefaultInstructions--) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline\#setDefaultInstructions-boolean-) is set. Default value for this property is **empty string**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Instructions to the signer that are displayed on signing the signature line. |

### getAllowComments() {#getAllowComments--}
```
public boolean getAllowComments()
```


Gets a value indicating that the signer can add comments in the Sign dialog. Default value for this property is **false**.

**Returns:**
boolean - A value indicating that the signer can add comments in the Sign dialog.
### setAllowComments(boolean value) {#setAllowComments-boolean-}
```
public void setAllowComments(boolean value)
```


Sets a value indicating that the signer can add comments in the Sign dialog. Default value for this property is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating that the signer can add comments in the Sign dialog. |

### getShowDate() {#getShowDate--}
```
public boolean getShowDate()
```


Gets a value indicating that sign date is shown in the signature line. Default value for this property is **true**.

**Returns:**
boolean - A value indicating that sign date is shown in the signature line.
### setShowDate(boolean value) {#setShowDate-boolean-}
```
public void setShowDate(boolean value)
```


Sets a value indicating that sign date is shown in the signature line. Default value for this property is **true**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating that sign date is shown in the signature line. |

### getId() {#getId--}
```
public UUID getId()
```


Gets identifier for this signature line.

This identifier can be associated with a digital signature, when signing document using [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil). This value must be unique and by default it is randomly generated new Guid.

**Returns:**
java.util.UUID - Identifier for this signature line.
### setId(UUID value) {#setId-java.util.UUID-}
```
public void setId(UUID value)
```


Sets identifier for this signature line.

This identifier can be associated with a digital signature, when signing document using [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil). This value must be unique and by default it is randomly generated new Guid.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.UUID | Identifier for this signature line. |

### getProviderId() {#getProviderId--}
```
public UUID getProviderId()
```


Gets signature provider identifier for this signature line. Default value is "\{00000000-0000-0000-0000-000000000000\}".

The cryptographic service provider (CSP) is an independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption. MS Office reserves the value of \{00000000-0000-0000-0000-000000000000\} for its default signature provider.

The GUID of the additionally installed provider should be obtained from the documentation shipped with the provider.

In addition, all the installed cryptographic providers are enumerated in windows registry. It can be found in the following path: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. There is a key name "CP Service UUID" which corresponds to a GUID of signature provider.

**Returns:**
java.util.UUID - Signature provider identifier for this signature line.
### setProviderId(UUID value) {#setProviderId-java.util.UUID-}
```
public void setProviderId(UUID value)
```


Sets signature provider identifier for this signature line. Default value is "\{00000000-0000-0000-0000-000000000000\}".

The cryptographic service provider (CSP) is an independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption. MS Office reserves the value of \{00000000-0000-0000-0000-000000000000\} for its default signature provider.

The GUID of the additionally installed provider should be obtained from the documentation shipped with the provider.

In addition, all the installed cryptographic providers are enumerated in windows registry. It can be found in the following path: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. There is a key name "CP Service UUID" which corresponds to a GUID of signature provider.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.UUID | Signature provider identifier for this signature line. |

### isSigned() {#isSigned--}
```
public boolean isSigned()
```


Indicates that signature line is signed by digital signature.

**Returns:**
boolean - The corresponding  boolean  value.
### isValid() {#isValid--}
```
public boolean isValid()
```


Indicates that signature line is signed by digital signature and this digital signature is valid.

**Returns:**
boolean - The corresponding  boolean  value.
