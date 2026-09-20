---
title: "Метод Aspose::Words::DocumentBase::ImportNode"
linktitle: "ImportNode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBase::ImportNode. Импортирует узел из другого документа в текущий документ в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words/documentbase/importnode/
---
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) method


Импортирует узел из другого документа в текущий документ.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Импортируемый узел. |
| isImportChildren | bool | **true** для импорта всех дочерних узлов рекурсивно; иначе **false**. |

### ReturnValue

Клонированный узел, принадлежащий текущему документу.
## Примечания


Этот метод использует параметр [UseDestinationStyles](../../importformatmode/) для разрешения форматирования.

Импорт узла создаёт копию исходного узла, принадлежащего импортирующему документу. Возвращённый узел не имеет родителя. Исходный узел не изменяется и не удаляется из оригинального документа.

Прежде чем узел из другого документа может быть вставлен в этот документ, его необходимо импортировать. Во время импорта свойства, специфичные для документа, такие как ссылки на стили и списки, переводятся из оригинального в импортирующий документ. После импорта узел может быть вставлен в соответствующее место документа с помощью [InsertBefore1()</see> или <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Если исходный узел уже принадлежит целевому документу, то просто создаётся глубокая копия исходного узла.

## Примеры



Показывает, как импортировать узел из одного документа в другой.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(srcDoc, u"Source document first paragraph text."));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(dstDoc, u"Destination document first paragraph text."));

// Каждый узел имеет родительский документ, которым является документ, содержащий узел.
// Вставка узла в документ, которому узел не принадлежит, вызовет исключение.
ASPOSE_ASSERT_NE(dstDoc, srcDoc->get_FirstSection()->get_Document());
ASSERT_THROW(static_cast<std::function<void()>>([&dstDoc, &srcDoc]() -> void
{
    dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(srcDoc->get_FirstSection());
})(), System::ArgumentException);

// Используйте метод ImportNode для создания копии узла, которая будет иметь документ
// который вызвал метод ImportNode, установленный в качестве нового документа‑владельца.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true));

ASPOSE_ASSERT_EQ(dstDoc, importedSection->get_Document());

// Теперь мы можем вставить узел в документ.
dstDoc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(importedSection);

ASSERT_EQ(u"Destination document first paragraph text.\r\nSource document first paragraph text.\r\n", dstDoc->ToString(Aspose::Words::SaveFormat::Text));
```

## См. также

* Class [Node](../../node/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) method


Импортирует узел из другого документа в текущий документ с параметром для управления форматированием.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Узел для импорта. |
| isImportChildren | bool | **true** для импорта всех дочерних узлов рекурсивно; иначе **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Указывает, как объединять конфликтующее форматирование стилей. |

### ReturnValue

Клонированный, импортированный узел. Узел принадлежит целевому документу, но не имеет родителя.
## Примечания


Эта перегрузка полезна для управления тем, как импортируются стили и форматирование списков.

Импорт узла создаёт копию исходного узла, принадлежащего импортирующему документу. Возвращённый узел не имеет родителя. Исходный узел не изменяется и не удаляется из оригинального документа.

Прежде чем узел из другого документа может быть вставлен в этот документ, его необходимо импортировать. Во время импорта свойства, специфичные для документа, такие как ссылки на стили и списки, переводятся из оригинального в импортирующий документ. После импорта узел может быть вставлен в соответствующее место документа с помощью [InsertBefore1()</see> или <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Если исходный узел уже принадлежит целевому документу, то просто создаётся глубокая копия исходного узла.

## Примеры



Показывает, как импортировать узел из исходного документа в целевой документ с определёнными параметрами.
```cpp
// Создайте два документа и добавьте символьный стиль в каждый документ.
// Настройте стили так, чтобы у них было одинаковое имя, но различное форматирование текста.
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> srcStyle = srcDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
srcStyle->get_Font()->set_Name(u"Courier New");
auto srcBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
srcBuilder->get_Font()->set_Style(srcStyle);
srcBuilder->Writeln(u"Source document text.");

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> dstStyle = dstDoc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"My style");
dstStyle->get_Font()->set_Name(u"Calibri");
auto dstBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
dstBuilder->get_Font()->set_Style(dstStyle);
dstBuilder->Writeln(u"Destination document text.");

// Импортируйте раздел из целевого документа в исходный документ, вызывая конфликт имён стилей.
// Если мы используем стили назначения, то импортированный исходный текст с тем же именем стиля
// будет принимать стиль назначения.
auto importedSection = System::ExplicitCast<Aspose::Words::Section>(dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::UseDestinationStyles));
ASSERT_EQ(dstStyle->get_Font()->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());
ASSERT_EQ(dstStyle->get_Name(), importedSection->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_StyleName());

// Если мы используем ImportFormatMode.KeepDifferentStyles, стиль источника сохраняется,
// и конфликт имён разрешается добавлением суффикса.
dstDoc->ImportNode(srcDoc->get_FirstSection(), true, Aspose::Words::ImportFormatMode::KeepDifferentStyles);
ASSERT_EQ(dstStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style")->get_Font()->get_Name());
ASSERT_EQ(srcStyle->get_Font()->get_Name(), dstDoc->get_Styles()->idx_get(u"My style_0")->get_Font()->get_Name());
```

## См. также

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBase::ImportNode(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Импортирует узел из другого документа в текущий документ с параметром для управления форматированием.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBase::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Узел для импорта. |
| isImportChildren | bool | **true** для импорта всех дочерних узлов рекурсивно; иначе **false**. |
| importFormatMode | Aspose::Words::ImportFormatMode | Указывает, как объединять конфликтующее форматирование стилей. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Позволяет указывать различные дополнительные параметры форматирования. |

### ReturnValue

Клонированный, импортированный узел. Узел принадлежит целевому документу, но не имеет родителя.
## Примечания


Эта перегрузка полезна для управления тем, как импортируются стили и форматирование списков.

Импорт узла создаёт копию исходного узла, принадлежащего импортирующему документу. Возвращённый узел не имеет родителя. Исходный узел не изменяется и не удаляется из оригинального документа.

Прежде чем узел из другого документа может быть вставлен в этот документ, его необходимо импортировать. Во время импорта свойства, специфичные для документа, такие как ссылки на стили и списки, переводятся из оригинального в импортирующий документ. После импорта узел может быть вставлен в соответствующее место документа с помощью [InsertBefore1()</see> или <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

Если исходный узел уже принадлежит целевому документу, то просто создаётся глубокая копия исходного узла.

## Примеры



Показывает, как импортировать узел с разрешением исходных цветовых тем фигур.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Перейдите к основному нижнему колонтитулу и вставьте форму, использующую цвета темы.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Импортируйте исходный нижний колонтитул в целевой документ с разрешёнными цветами темы,
// чтобы форма сохраняла свой фактический цвет из исходного документа.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## См. также

* Class [Node](../../node/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
