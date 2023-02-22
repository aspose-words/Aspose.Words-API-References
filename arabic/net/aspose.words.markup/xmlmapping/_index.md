---
title: Class XmlMapping
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Markup.XmlMapping فصل. يحدد المعلومات المستخدمة لإنشاء تعيين بين علامة المستند المهيكلة parent وعنصر XML المخزن في جزء بيانات XML مخصص في المستند.
type: docs
weight: 3860
url: /ar/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

يحدد المعلومات المستخدمة لإنشاء تعيين بين علامة المستند المهيكلة parent وعنصر XML المخزن في جزء بيانات XML مخصص في المستند.

```csharp
public class XmlMapping
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | إرجاع جزء بيانات XML المخصص الذي تم تعيين علامة المستند المهيكلة الأصلية إليه. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | عوائد **حقيقي** إذا تم تعيين علامة المستند المهيكل الأصلي بنجاح إلى بيانات XML. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | إرجاع تعيينات بادئة مساحة اسم XML لتقييم ملف[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | يحدد معرف بيانات XML المخصص لجزء بيانات XML المخصص والذي يجب استخدامه لتقييم[`XPath`](./xpath/) التعبير . |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | إرجاع تعبير XPath ، الذي تم تقييمه للعثور على XML node المخصص الذي تم تعيينه إلى علامة المستند المهيكلة الأصل. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | حذف تعيين المستند الأصلي المهيكل إلى بيانات XML. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(CustomXmlPart, string, string) | تعيين تعيين بين علامة المستند المهيكلة الأصلية وعقدة XML لجزء بيانات XML المخصص. |

### أمثلة

يوضح كيفية تعيين تعيينات XML لأجزاء XML المخصصة.

```csharp
Document doc = new Document();

// إنشاء جزء XML يحتوي على نص وإضافته إلى مجموعة CustomXmlPart الخاصة بالمستند.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>", 
    Encoding.UTF8.GetString(xmlPart.Data));

// قم بإنشاء علامة مستند منظم تعرض محتويات CustomXmlPart الخاصة بنا.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// تعيين تعيين لعلامة المستند المنظمة الخاصة بنا. هذا التعيين سوف يوجه
// علامة المستند المهيكلة الخاصة بنا لعرض جزء من محتويات نص جزء XML الذي يشير إليه XPath.
// في هذه الحالة ، ستكون محتويات الثانية "< text >" عنصر أول "< root >" العنصر: "عنصر النص رقم 2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema ") ;

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema '"، tag.XmlMapping.PrefixMappings) ;

// أضف علامة المستند المهيكلة إلى المستند لعرض المحتوى من الجزء المخصص لدينا.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)


