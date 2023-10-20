---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Markup.IStructuredDocumentTag واجهه المستخدم. واجهة لتعريف البيانات المشتركةStructuredDocumentTag وStructuredDocumentTagRangeStart  في C#.
type: docs
weight: 3970
url: /ar/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

واجهة لتعريف البيانات المشتركة[`StructuredDocumentTag`](../structureddocumenttag/) و[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | الحصول على أو تعيين لون علامة المستند المنظمة. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | يحدد معرفًا رقميًا ثابتًا فريدًا للقراءة فقط لهذا الغرض**المعاملة الخاصة والتفضيلية**. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | يحدد ما إذا كان محتوى هذا**المعاملة الخاصة والتفضيلية** يجب تفسيره على أنه يحتوي على العنصر النائب text (على عكس محتويات النص العادي ضمن المعاملة الخاصة والتفضيلية). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | يحصل على المستوى الذي عنده**المعاملة الخاصة والتفضيلية** يحدث في شجرة المستندات. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | عند التعيين على "صحيح"، ستمنع هذه الخاصية المستخدم من حذفها**المعاملة الخاصة والتفضيلية** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | عند التعيين على "صحيح"، ستمنع هذه الخاصية المستخدم من تحرير محتويات هذه الخاصية**المعاملة الخاصة والتفضيلية** . |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | يحصل على[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)يحتوي على نص عنصر نائب يجب عرضه عندما تكون محتويات تشغيل SDT فارغة، عنصر XML المعين المرتبط فارغ كما هو محدد عبر[`XmlMapping`](./xmlmapping/) element أو[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) العنصر صحيح |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | الحصول على أو تعيين اسم[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) تحتوي على نص نائب. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | يحصل على نوع من هذا**علامة الوثيقة المنظمة** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | يحدد علامة مرتبطة بعقدة SDT الحالية. لا يمكن أن تكون فارغة. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | يحدد الاسم المألوف المرتبط بهذا**المعاملة الخاصة والتفضيلية** . لا يمكن أن يكون فارغًا. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | يحصل على سلسلة تمثل XML الموجود داخل العقدة في ملفFlatOpc التنسيق. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | الحصول على كائن يمثل تعيين علامة المستند المنظمة هذه إلى بيانات XML في جزء XML مخصص من المستند الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [IsRanged](../../aspose.words.markup/istructureddocumenttag/isranged/)() | إرجاع صحيح إذا كان هذا المثيل عبارة عن علامة مستند منظمة ذات نطاق. |
| [StructuredDocumentTagNode](../../aspose.words.markup/istructureddocumenttag/structureddocumenttagnode/)() | إرجاع كائن العقدة الذي ينفذ هذه الواجهة. |

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
