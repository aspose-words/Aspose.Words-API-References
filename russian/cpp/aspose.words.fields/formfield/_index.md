---
title: "Aspose::Words::Fields::FormField класс"
linktitle: "FormField"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FormField класс. Представляет отдельное поле формы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 112000
url: /ru/cpp/aspose.words.fields/formfield/
---
## FormField class


Представляет отдельное поле формы. Чтобы узнать больше, посетите статью документации [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormField : public Aspose::Words::SpecialChar
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создаёт дубликат узла. |
| [get_CalculateOnExit](./get_calculateonexit/)() | True, если ссылки на указанный поле формы автоматически обновляются при выходе из поля. |
| [get_CheckBoxSize](./get_checkboxsize/)() | Получает или задает размер флажка в пунктах. Действует только когда [IsCheckBoxExactSize](./get_ischeckboxexactsize/) **true**. |
| [get_Checked](./get_checked/)() | Получает или задает состояние отметки флажка формы. Значение по умолчанию для этого свойства **false**. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| [get_Default](./get_default/)() | Получает или задает значение по умолчанию флажка формы. Значение по умолчанию для этого свойства **false**. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_DropDownItems](./get_dropdownitems/)() | Обеспечивает доступ к элементам раскрывающегося поля формы. |
| [get_DropDownSelectedIndex](./get_dropdownselectedindex/)() | Получает индекс, указывающий текущий выбранный элемент в раскрывающемся поле формы. |
| [get_Enabled](./get_enabled/)() | Истина, если поле формы включено. |
| [get_EntryMacro](./get_entrymacro/)() | Возвращает или задает имя макроса входа для поля формы. |
| [get_ExitMacro](./get_exitmacro/)() | Возвращает или задает имя макроса выхода для поля формы. |
| [get_Font](../../aspose.words/inline/get_font/)() | Предоставляет доступ к форматированию шрифта этого объекта. |
| [get_HelpText](./get_helptext/)() | Возвращает или задает текст, отображаемый в диалоговом окне сообщения, когда поле формы имеет фокус и пользователь нажимает F1. |
| [get_IsCheckBoxExactSize](./get_ischeckboxexactsize/)() | Получает или задает логическое значение, указывающее, является ли размер текстового поля автоматическим или задан явно. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Возвращает **true**, если этот узел может содержать другие узлы. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Возвращает true, если этот объект был удалён в Microsoft Word при включённом отслеживании изменений. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включённом отслеживании изменений. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Возвращает true, если этот объект был вставлен в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Возвращает **true**, если этот объект был перемещён (удалён) в Microsoft Word при включённом отслеживании изменений. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Возвращает **true**, если этот объект был перемещён (вставлен) в Microsoft Word при включённом отслеживании изменений. |
| [get_MaxLength](./get_maxlength/)() | Максимальная длина текстового поля. Ноль, если длина не ограничена. |
| [get_Name](./get_name/)() | Получает или задает имя поля формы. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает [FormField](../../aspose.words/nodetype/). |
| [get_OwnHelp](./get_ownhelp/)() | Указывает источник текста, отображаемого в диалоговом окне сообщения, когда поле формы имеет фокус и пользователь нажимает F1. |
| [get_OwnStatus](./get_ownstatus/)() | Указывает источник текста, отображаемого в строке состояния, когда поле формы имеет фокус. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Получает родительский [Paragraph](../../aspose.words/paragraph/) этого узла. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Возвращает объект [Range](../../aspose.words/range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_Result](./get_result/)() | Получает или задает строку, представляющую результат этого поля формы. |
| [get_StatusText](./get_statustext/)() | Возвращает или задает текст, отображаемый в строке состояния, когда поле формы имеет фокус. |
| [get_TextInputDefault](./get_textinputdefault/)() | Получает или задает строку по умолчанию или выражение вычисления текстового поля формы. |
| [get_TextInputFormat](./get_textinputformat/)() | Возвращает или задает форматирование текста для текстового поля формы. |
| [get_TextInputType](./get_textinputtype/)() | Получает тип текстового поля формы. |
| [get_Type](./get_type/)() | Возвращает тип поля формы. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Возвращает первого предка указанного [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Получает специальный символ, который представляет этот узел. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родительского узла. |
| [RemoveField](./removefield/)() | Удаляет полностью поле формы, а не только специальный символ поля формы. |
| [set_CalculateOnExit](./set_calculateonexit/)(bool) | Сеттер для [Aspose::Words::Fields::FormField::get_CalculateOnExit](./get_calculateonexit/). |
| [set_CheckBoxSize](./set_checkboxsize/)(double) | Сеттер для [Aspose::Words::Fields::FormField::get_CheckBoxSize](./get_checkboxsize/). |
| [set_Checked](./set_checked/)(bool) | Сеттер для [Aspose::Words::Fields::FormField::get_Checked](./get_checked/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Default](./set_default/)(bool) | Сеттер для [Aspose::Words::Fields::FormField::get_Default](./get_default/). |
| [set_DropDownSelectedIndex](./set_dropdownselectedindex/)(int32_t) | Задает индекс, указывающий текущий выбранный элемент в раскрывающемся поле формы. |
| [set_Enabled](./set_enabled/)(bool) | Истина, если поле формы включено. |
| [set_EntryMacro](./set_entrymacro/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FormField::get_EntryMacro](./get_entrymacro/). |
| [set_ExitMacro](./set_exitmacro/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FormField::get_ExitMacro](./get_exitmacro/). |
| [set_HelpText](./set_helptext/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FormField::get_HelpText](./get_helptext/). |
| [set_IsCheckBoxExactSize](./set_ischeckboxexactsize/)(bool) | Сеттер для [Aspose::Words::Fields::FormField::get_IsCheckBoxExactSize](./get_ischeckboxexactsize/). |
| [set_MaxLength](./set_maxlength/)(int32_t) | Максимальная длина текстового поля. Ноль, если длина не ограничена. |
| [set_Name](./set_name/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FormField::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_OwnHelp](./set_ownhelp/)(bool) | Сеттер для [Aspose::Words::Fields::FormField::get_OwnHelp](./get_ownhelp/). |
| [set_OwnStatus](./set_ownstatus/)(bool) | Сеттер для [Aspose::Words::Fields::FormField::get_OwnStatus](./get_ownstatus/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Result](./set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FormField::get_Result](./get_result/). |
| [set_StatusText](./set_statustext/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FormField::get_StatusText](./get_statustext/). |
| [set_TextInputDefault](./set_textinputdefault/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FormField::get_TextInputDefault](./get_textinputdefault/). |
| [set_TextInputFormat](./set_textinputformat/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FormField::get_TextInputFormat](./get_textinputformat/). |
| [set_TextInputType](./set_textinputtype/)(Aspose::Words::Fields::TextFormFieldType) | Устанавливает тип текстового поля формы. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTextInputValue](./settextinputvalue/)(const System::SharedPtr\<System::Object\>\&) | Применяет текстовый формат, указанный в [TextInputFormat](./get_textinputformat/), и сохраняет значение в [Result](./get_result/). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


Microsoft Word предоставляет следующие поля формы: флажок, ввод текста и раскрывающийся список (комбобокс).

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[FormField](./) is represented in a document by a special character and positioned as a character within a line of text.

Полное поле формы в документе Word представляет собой сложную структуру, состоящую из нескольких узлов: начало поля, код поля, такой как FORMTEXT, данные поля формы, разделитель поля, результат поля, конец поля и закладка. Чтобы программно создавать поля формы в документе Word, используйте [InsertCheckBox()](../), [InsertTextInput()](../) и [InsertComboBox()](../), которые гарантируют, что все узлы поля формы созданы в правильном порядке и находятся в надлежащем состоянии.

## Примеры



Показывает, как вставить комбобокс.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Вставьте комбобокс, который позволит пользователю выбрать вариант из набора строк.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Поле формы будет отображаться в виде HTML‑тега "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```


Показывает, как отформатировать весь [FormField](./), включая значение поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(0);
formField->get_Font()->set_Bold(true);
formField->get_Font()->set_Size(24);
formField->get_Font()->set_Color(System::Drawing::Color::get_Red());

formField->set_Result(u"Aspose.FormField");

doc = Aspose::Words::ApiExamples::DocumentHelper::SaveOpen(doc);

System::SharedPtr<Aspose::Words::Run> formFieldRun = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1);

ASSERT_EQ(u"Aspose.FormField", formFieldRun->get_Text());
ASPOSE_ASSERT_EQ(true, formFieldRun->get_Font()->get_Bold());
ASPOSE_ASSERT_EQ(24, formFieldRun->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), formFieldRun->get_Font()->get_Color().ToArgb());
```

## См. также

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
