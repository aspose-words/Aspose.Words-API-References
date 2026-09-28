---
title: "Aspose::Words::Paragraph класс"
linktitle: "Paragraph"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Paragraph класс. Представляет абзац текста. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 47000
url: /ru/cpp/aspose.words/paragraph/
---
## Paragraph class


Представляет абзац текста. Чтобы узнать больше, посетите статью документации [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class Paragraph : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IParaAttrSource,
                  public Aspose::Words::IRunAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения конца абзаца документа. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения начала абзаца документа. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendField](./appendfield/)(Aspose::Words::Fields::FieldType, bool) | Добавляет поле к этому абзацу. |
| [AppendField](./appendfield/)(const System::String\&) | Добавляет поле к этому абзацу. |
| [AppendField](./appendfield/)(const System::String\&, const System::String\&) | Добавляет поле к этому абзацу. |
| [Clone](../node/clone/)(bool) | Создаёт дубликат узла. |
| [get_BreakIsStyleSeparator](./get_breakisstyleseparator/)() | Истина, если разрыв этого абзаца является разделителем [Style](../style/). Разделитель стиля позволяет одному абзацу состоять из частей, имеющих разные стили абзаца. |
| [get_Count](../compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| virtual [get_Document](../node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_FrameFormat](./get_frameformat/)() | Предоставляет доступ к свойствам форматирования рамки. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений. |
| [get_IsEndOfCell](./get_isendofcell/)() | Истина, если этот абзац является последним абзацем в [Cell](../../aspose.words.tables/cell/); иначе — ложь. |
| [get_IsEndOfDocument](./get_isendofdocument/)() | Истина, если этот абзац является последним абзацем в последнем разделе документа. |
| [get_IsEndOfHeaderFooter](./get_isendofheaderfooter/)() | Истина, если этот абзац является последним абзацем в [HeaderFooter](../headerfooter/) (основная текстовая история) [Section](../section/); иначе — ложь. |
| [get_IsEndOfSection](./get_isendofsection/)() | Истина, если этот абзац является последним абзацем в [Body](../body/) (основная текстовая история) [Section](../section/); иначе — ложь. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включённом отслеживании изменений. |
| [get_IsInCell](./get_isincell/)() | Истина, если этот абзац является непосредственным дочерним элементом [Cell](../../aspose.words.tables/cell/); иначе — ложь. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Возвращает true, если этот объект был вставлен в Microsoft Word при включённом отслеживании изменений. |
| [get_IsListItem](./get_islistitem/)() | Истина, когда абзац является элементом маркированного или нумерованного списка в оригинальной редакции. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Возвращает **true**, если этот объект был перемещён (удалён) в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Возвращает **true**, если этот объект был перемещён (вставлен) в Microsoft Word при включённом отслеживании изменений. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_ListFormat](./get_listformat/)() | Предоставляет доступ к свойствам форматирования списка абзаца. |
| [get_ListLabel](./get_listlabel/)() | Получает объект [ListLabel](./get_listlabel/), который предоставляет доступ к значению нумерации списка и его форматированию для этого абзаца. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает [Paragraph](../nodetype/). |
| [get_ParagraphBreakFont](./get_paragraphbreakfont/)() | Предоставляет доступ к форматированию шрифта символа разрыва абзаца. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Предоставляет доступ к свойствам форматирования абзаца. |
| [get_ParentNode](../node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_ParentSection](./get_parentsection/)() | Получает родительский [Section](../section/) абзаца. |
| [get_ParentStory](./get_parentstory/)() | Получает родительскую историю уровня раздела, которой может быть [Body](../body/) или [HeaderFooter](../headerfooter/). |
| [get_PreviousSibling](../node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Возвращает объект [Range](../range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_Runs](./get_runs/)() | Предоставляет доступ к типизированной коллекции фрагментов текста внутри абзаца. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Получает первого предка указанного [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Возвращает N‑й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEffectiveTabStops](./geteffectivetabstops/)() | Возвращает массив всех табуляций, применённых к этому абзацу, включая косвенно применённые стилями или списками. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Обеспечивает поддержку итерации в стиле foreach по дочерним узлам этого узла. |
| [GetText](./gettext/)() override | Получает текст этого абзаца, включая символ конца абзаца. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Вставляет поле в этот абзац. |
| [InsertField](./insertfield/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Вставляет поле в этот абзац. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Вставляет поле в этот абзац. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Объединяет участки текста с одинаковым форматированием в абзаце. |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) | Объединяет участки текста с одинаковым форматированием в абзаце. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [Paragraph](./paragraph/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Инициализирует новый экземпляр класса [Paragraph](./). |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../node/remove/)() | Удаляет себя из родительского узла. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Удаляет все дочерние узлы [SmartTag](../../aspose.words.markup/smarttag/) текущего узла. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Выбирает список узлов, соответствующих XPath-выражению. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Выбирает первый [Node](../node/), который соответствует выражению XPath. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


[Paragraph](./) is a block-level node and can be a child of classes derived from [Story](../story/) or [InlineStory](../inlinestory/).

[Paragraph](./) can contain any number of inline-level nodes and bookmarks.

Полный список дочерних узлов, которые могут находиться внутри абзаца, состоит из [BookmarkStart](../bookmarkstart/), [BookmarkEnd](../bookmarkend/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Comment](../comment/), [Footnote](../../aspose.words.notes/footnote/), [Run](../run/), [SpecialChar](../specialchar/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [SmartTag](../../aspose.words.markup/smarttag/).

Корректный абзац в Microsoft Word всегда заканчивается символом разрыва абзаца, а минимальный корректный абзац состоит лишь из разрыва абзаца. Класс [Paragraph](./) автоматически добавляет соответствующий символ разрыва абзаца в конце, и этот символ не является частью дочерних узлов [Paragraph](./), поэтому [Paragraph](./) может быть пустым.

Не включайте символы конца абзаца [ParagraphBreak](../controlchar/paragraphbreak/) или конца ячейки [Cell](../controlchar/cell/) в текст абзаца, так как это может сделать абзац недействительным при открытии документа в Microsoft Word.

## Примеры



Показывает, как вручную построить документ Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Пустой документ содержит один раздел, одно тело и один абзац.
// Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы,
// и в результате получите узел документа без дочерних элементов.
doc->RemoveAllChildren();

// У этого документа теперь нет составных дочерних узлов, к которым мы могли бы добавить содержимое.
// Если мы захотим отредактировать его, нам потребуется заново заполнить его коллекцию узлов.
// Сначала создайте новый раздел, а затем добавьте его как дочерний элемент к корневому узлу документа.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Установите некоторые свойства разметки страницы для раздела.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Разделу требуется тело, которое будет содержать и отображать всё его содержимое
// на странице между заголовком и нижним колонтитулом раздела.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Создайте абзац, задайте некоторые свойства форматирования и затем добавьте его как дочерний элемент к телу.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Наконец, добавьте некоторое содержимое в документ. Создайте объект Run,
// задайте его внешний вид и содержимое, а затем добавьте его как дочерний элемент к абзацу.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## См. также

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
