---
title: XmlMapping.StoreItemId
second_title: Aspose.Words لمراجع .NET API
description: XmlMapping ملكية. يحدد معرف بيانات XML المخصص لجزء بيانات XML المخصص والذي يجب استخدامه لتقييمXPath التعبير.
type: docs
weight: 40
url: /ar/net/aspose.words.markup/xmlmapping/storeitemid/
---
## XmlMapping.StoreItemId property

يحدد معرف بيانات XML المخصص لجزء بيانات XML المخصص والذي يجب استخدامه لتقييم[`XPath`](../xpath/) التعبير.

```csharp
public string StoreItemId { get; }
```

### أمثلة

يوضح كيفية الحصول على معرف بيانات XML المخصص لجزء XML.

```csharp
Document doc = new Document(MyDir + "Custom XML part in structured document tag.docx");

// تحتوي علامات المستندات المنظمة على معرفات في شكل معرفات GUID.
StructuredDocumentTag tag = (StructuredDocumentTag) doc.GetChild(NodeType.StructuredDocumentTag, 0, true);

Assert.AreEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.XmlMapping.StoreItemId);
```

### أنظر أيضا

* class [XmlMapping](../)
* مساحة الاسم [Aspose.Words.Markup](../../xmlmapping/)
* المجسم [Aspose.Words](../../../)


