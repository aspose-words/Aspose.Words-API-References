---
title: "Aspose::Words::Markup 命名空间"
linktitle: "Aspose::Words::Markup"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup 命名空间。Aspose.Words.Markup 命名空间包含表示文档中客户自定义语义的类：智能标签、自定义 XML 和结构化文档标签（内容控件），适用于 C++。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.markup/
---

该 **Aspose.Words.Markup** 命名空间包含表示文档中客户自定义语义的类：智能标签、自定义 XML 和结构化文档标签（内容控件）。

## 类

| 类 | 描述 |
| --- | --- |
| [CustomPart](./custompart/) | 表示未被 ISO/IEC 29500 标准定义的自定义（任意内容）部件。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [CustomPartCollection](./custompartcollection/) | 表示一组 [CustomPart](./custompart/) 对象。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [CustomXmlPart](./customxmlpart/) | 表示自定义 XML 数据存储部件（包内的自定义 XML 数据）。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [CustomXmlPartCollection](./customxmlpartcollection/) | 表示一组自定义 XML 部件。这些项是 [CustomXmlPart](./customxmlpart/) 对象。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [CustomXmlProperty](./customxmlproperty/) | 表示单个自定义 XML 属性或智能标签属性。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [CustomXmlPropertyCollection](./customxmlpropertycollection/) | 表示一组自定义 XML 属性或智能标签属性。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [CustomXmlSchemaCollection](./customxmlschemacollection/) | 一组表示与自定义 XML 部件关联的 XML 架构的字符串。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [SdtListItem](./sdtlistitem/) | 此元素指定父级 [ComboBox](./sdttype/) 或 [DropDownList](./sdttype/) 结构化文档标签中的单个列表项。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [SdtListItemCollection](./sdtlistitemcollection/) | 提供对结构化文档标签的 [SdtListItem](./sdtlistitem/) 元素的访问。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [SmartTag](./smarttag/) | 此元素指定段落中一个或多个内联结构（运行、图像、字段等）周围的智能标签的存在。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [StructuredDocumentTag](./structureddocumenttag/) | 表示文档中的结构化文档标签（SDT 或内容控件）。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [StructuredDocumentTagCollection](./structureddocumenttagcollection/) | 一组 [IStructuredDocumentTag](./istructureddocumenttag/) 实例，表示指定范围内的结构化文档标签。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/) | 表示 **ranged** 结构化文档标签的结束，该标签接受多节内容。另请参阅 [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) 节点。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) | 表示 **ranged** 结构化文档标签的开始，该标签接受多节内容。另请参阅 [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/)。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
| [XmlMapping](./xmlmapping/) | 指定用于在文档中建立父结构化文档标签与存储在自定义 XML 数据部件中的 XML 元素之间映射的信息。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。 |
## 接口

| 接口 | 描述 |
| --- | --- |
| [IStructuredDocumentTag](./istructureddocumenttag/) | 用于为 [StructuredDocumentTag](./structureddocumenttag/) 和 [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) 定义通用数据的接口。 |
## Enums

| 枚举 | 描述 |
| --- | --- |
| [MarkupLevel](./markuplevel/) | 指定特定 [StructuredDocumentTag](./structureddocumenttag/) 可以出现的文档树层级。 |
| [SdtAppearance](./sdtappearance/) | 指定结构化文档标签的外观。 |
| [SdtCalendarType](./sdtcalendartype/) | 指定在 Office Open XML 文档中可用于指定 [CalendarType](./structureddocumenttag/get_calendartype/) 的可能日历类型。 |
| [SdtDateStorageFormat](./sdtdatestorageformat/) | 指定当日期 SDT 绑定到文档数据存储中的 XML 节点时，日期的存储/检索方式。 |
| [SdtType](./sdttype/) | 指定结构化文档标签 (SDT) 节点的类型。 |
