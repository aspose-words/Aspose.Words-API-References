---
title: Class FormField
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FormField сорт. Представляет одно поле формы.
type: docs
weight: 2620
url: /ru/net/aspose.words.fields/formfield/
---
## FormField class

Представляет одно поле формы.

Чтобы узнать больше, посетите[Работа с полями формы](https://docs.aspose.com/words/net/working-with-form-fields/) статья документации.

```csharp
public class FormField : SpecialChar
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | True, если ссылки на указанное поле формы автоматически обновляются при выходе из поля. |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | Получает или задает размер флажка в пунктах. Имеет эффект только тогда, когда[`IsCheckBoxExactSize`](./ischeckboxexactsize/) является`истинный` . |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | Получает или задает проверенный статус поля формы флажка. Значение по умолчанию для этого свойства:`ЛОЖЬ` . |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | Получает или задает значение по умолчанию для поля формы флажка. Значение по умолчанию для этого свойства:`ЛОЖЬ` . |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | Обеспечивает доступ к элементам поля раскрывающейся формы. |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | Получает или задает индекс, определяющий текущий выбранный элемент в поле раскрывающейся формы. |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | True, если поле формы включено. |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | Возвращает или задает имя макроса записи для поля формы. |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | Возвращает или задает имя макроса выхода для поля формы. |
| [Font](../../aspose.words/inline/font/) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | Возвращает или задает текст, который отображается в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает F1. |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | Получает или задает логическое значение, указывающее, является ли размер текстового поля автоматическим или заданным явно. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Возвращает`истинный` если этот узел может содержать другие узлы. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Возвращает`истинный` если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Возвращает`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | Максимальная длина текстового поля. Ноль, если длина не ограничена. |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | Получает или задает имя поля формы. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | ВозвращаетFormField . |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | Указывает источник текста, который отображается в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает F1. |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | Указывает источник текста, который отображается в строке состояния, когда поле формы имеет фокус. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Получает родительский элемент[`Paragraph`](../../aspose.words/paragraph/) этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../../aspose.words/range/) объект, представляющий часть документа, содержащуюся в этом узле. |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | Получает или задает строку, представляющую результат этого поля формы. |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | Возвращает или задает текст, который отображается в строке состояния, когда поле формы находится в фокусе. |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | Получает или задает строку по умолчанию или выражение вычисления поля текстовой формы. |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | Возвращает или задает форматирование текста для поля текстовой формы. |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | Получает или задает тип поля текстовой формы. |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | Возвращает тип поля формы. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(DocumentVisitor) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Получает специальный символ, который представляет этот узел. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя от родителя. |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | Удаляет все поле формы, а не только специальный символ поля формы. |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(object) | Применяет текстовый формат, указанный в[`TextInputFormat`](./textinputformat/) и сохраняет значение в[`Result`](./result/) . |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

Microsoft Word предоставляет следующие поля формы: флажок, ввод текста и раскрывающийся список (поле со списком).

`FormField`является встроенным узлом и может быть только дочерним элементом[`Paragraph`](../../aspose.words/paragraph/).

`FormField` представлен в документе специальным символом and , позиционируемым как символ внутри строки текста.

Полное поле формы в документе Word представляет собой сложную структуру, представленную несколькими узлами : начало поля, код поля, например FORMTEXT, данные поля формы, разделитель полей, результат поля , конец поля и закладка. Чтобы программно создать поля формы в документе Word, используйте .[`InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/) , [`InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/) and [`InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/) Which убедитесь, что все узлы полей формы созданы в правильном порядке и в подходящем состоянии.

### Примеры

Показывает, как форматировать весь FormField, включая значение поля.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[0];
formField.Font.Bold = true;
formField.Font.Size = 24;
formField.Font.Color = Color.Red;

formField.Result = "Aspose.FormField";

doc = DocumentHelper.SaveOpen(doc);

Run formFieldRun = doc.FirstSection.Body.FirstParagraph.Runs[1];

Assert.AreEqual("Aspose.FormField", formFieldRun.Text);
Assert.AreEqual(true, formFieldRun.Font.Bold);
Assert.AreEqual(24, formFieldRun.Font.Size);
Assert.AreEqual(Color.Red.ToArgb(), formFieldRun.Font.Color.ToArgb());
```

Показывает, как вставить поле со списком.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Вставляем поле со списком, которое позволит пользователю выбрать вариант из коллекции строк.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Поле формы появится в виде html-тега select.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Смотрите также

* class [SpecialChar](../../aspose.words/specialchar/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)


