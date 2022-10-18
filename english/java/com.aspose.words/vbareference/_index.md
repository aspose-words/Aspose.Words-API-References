---
title: VbaReference
second_title: Aspose.Words for Java API Reference
description: Implements a reference to an Automation type library or VBA project.
type: docs
weight: 597
url: /java/com.aspose.words/vbareference/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public abstract class VbaReference implements Cloneable
```

Implements a reference to an Automation type library or VBA project.

To learn more, visit the **Working with VBA Macros** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [VbaReference()](#VbaReference--) |  |
## Methods

| Method | Description |
| --- | --- |
| [getType()](#getType--) | Gets [VbaReferenceType](../../com.aspose.words/vbareferencetype) object that indicates the type of reference that a VbaReference object represents. |
| [getLibId()](#getLibId--) | Gets a string value containing the identifier of an Automation type library. |
### VbaReference() {#VbaReference--}
```
public VbaReference()
```


### getType() {#getType--}
```
public abstract int getType()
```


Gets [VbaReferenceType](../../com.aspose.words/vbareferencetype) object that indicates the type of reference that a VbaReference object represents.

**Returns:**
int - \{[VbaReferenceType](../../com.aspose.words/vbareferencetype) object that indicates the type of reference that a VbaReference object represents. The returned value is one of [VbaReferenceType](../../com.aspose.words/vbareferencetype) constants.
### getLibId() {#getLibId--}
```
public abstract String getLibId()
```


Gets a string value containing the identifier of an Automation type library. Depending on reference type, the value of this property can be:

 *  a LibidReference specified at 2.1.1.8 LibidReference of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
 *  a ProjectReference specified at 2.1.1.12 ProjectReference of [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office\_file\_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131

**Returns:**
java.lang.String - A string value containing the identifier of an Automation type library.
