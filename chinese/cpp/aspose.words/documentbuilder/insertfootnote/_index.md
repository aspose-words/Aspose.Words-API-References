---
title: "Aspose::Words::DocumentBuilder::InsertFootnote 方法"
linktitle: "InsertFootnote"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertFootnote 方法。向文档中插入脚注或尾注（C++）。"
type: docs
weight: 35000
url: /zh/cpp/aspose.words/documentbuilder/insertfootnote/
---
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&) method


在文档中插入脚注或尾注。

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | 指定是否插入脚注或尾注。 |
| footnoteText | const System::String\& | 指定脚注的文本。 |

### ReturnValue

返回刚创建的脚注对象。

## 示例



展示如何使用脚注和尾注引用文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一些文本，并使用脚注标记，默认将 IsAuto 属性设置为 "true"，
// 因此正文中看到的标记将自动编号为 "1"，
// 并且脚注将出现在页面底部。
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// 插入更多文本，并使用自定义引用标记的尾注进行标记，
// 该标记将代替数字 "2" 使用，并将 "IsAuto" 设置为 false。
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// 脚注始终出现在其引用文本的底部，
// 因此此分页符不会影响脚注。
// 另一方面，尾注始终位于文档的末尾
// 因此此分页符会将尾注推到下一页。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```

## 另见

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) method


在文档中插入脚注或尾注。

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText, const System::String &referenceMark)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | 指定是否插入脚注或尾注。 |
| footnoteText | const System::String\& | 指定脚注的文本。 |
| referenceMark | const System::String\& | 指定脚注的自定义引用标记。 |

### ReturnValue

返回刚创建的脚注对象。

## 示例



展示如何使用脚注和尾注引用文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一些文本，并使用脚注标记，默认将 IsAuto 属性设置为 "true"，
// 因此正文中看到的标记将自动编号为 "1"，
// 并且脚注将出现在页面底部。
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// 插入更多文本，并使用自定义引用标记的尾注进行标记，
// 该标记将代替数字 "2" 使用，并将 "IsAuto" 设置为 false。
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// 脚注始终出现在其引用文本的底部，
// 因此此分页符不会影响脚注。
// 另一方面，尾注始终位于文档的末尾
// 因此此分页符会将尾注推到下一页。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```

## 另见

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
