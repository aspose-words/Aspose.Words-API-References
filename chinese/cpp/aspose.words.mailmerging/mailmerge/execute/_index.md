---
title: "Aspose::Words::MailMerging::MailMerge::Execute 方法"
linktitle: "执行"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::MailMerge::Execute 方法。在 C++ 中对单条记录执行邮件合并操作。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge::Execute(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) method


对单条记录执行邮件合并操作。

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::ArrayPtr<System::String> &fieldNames, const System::ArrayPtr<System::SharedPtr<System::Object>> &values)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| fieldNames | const System::ArrayPtr\<System::String\>\& | 合并字段名称的数组。字段名称不区分大小写。如果遇到文档中未找到的字段名称，将被忽略。 |
| 值 | const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\& | 要插入合并字段的值数组。此数组中的元素数量必须与 *fieldNames* 中的元素数量相同。 |
## 备注


使用此方法将来自对象数组的值填充到文档中的邮件合并字段。

此方法仅合并单条记录的数据。字段名数组和数值数组表示单条记录的数据。

此方法不使用邮件合并区域。

此方法忽略 [RemoveUnusedRegions](../../mailmergecleanupoptions/) 选项。

## 示例



展示如何将来自 URI 的图像作为邮件合并数据合并到 MERGEFIELD。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 带有 \"Image:\" 标记的 MERGEFIELD 将在邮件合并期间接收图像。
// 在 \"Image:\" 标记中冒号后的字符串对应列名
// 在数据源中，其单元格包含图像文件的 URI。
builder->InsertField(u"MERGEFIELD  Image:logo_FromWeb ");
builder->InsertField(u"MERGEFIELD  Image:logo_FromFileSystem ");

// 创建一个包含我们将要合并的图像 URI 的数据源。
// URI 可以是指向图像的网络 URL，或本地文件系统中图像文件的文件名。
System::ArrayPtr<System::String> columns = System::MakeArray<System::String>({u"logo_FromWeb", u"logo_FromFileSystem"});
System::ArrayPtr<System::SharedPtr<System::Object>> URIs = System::MakeArray<System::SharedPtr<System::Object>>({System::ExplicitCast<System::Object>(get_ImageUrl()), System::ExplicitCast<System::Object>(get_ImageDir() + u"Logo.jpg")});

// 对包含一行的数据源执行邮件合并。
doc->get_MailMerge()->Execute(columns, URIs);

doc->Save(get_ArtifactsDir() + u"MailMergeEvent.ImageFromUrl.docx");
```

## 另见

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::Execute(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


从自定义数据源执行邮件合并。

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 数据源 | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | 实现自定义邮件合并数据源接口的对象。 |
## 备注


使用此方法将来自任何数据源（如列表、哈希表或对象）的值填充到文档中的邮件合并字段。您需要编写实现 [IMailMergeDataSource](../../imailmergedatasource/) 接口的自定义类。

仅当 [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) 为 **false** 时才能使用此方法，即您不需要从右到左语言（如阿拉伯语或希伯来语）的兼容性。

此方法忽略 [RemoveUnusedRegions](../../mailmergecleanupoptions/) 选项。

## 另见

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
