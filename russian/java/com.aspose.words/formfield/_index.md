---
title: FormField
second_title: Справочник по API Aspose.Words для Java
description: Представляет одно поле формы.
type: docs
weight: 296
url: /ru/java/com.aspose.words/formfield/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.Inline](../../com.aspose.words/inline), [com.aspose.words.SpecialChar](../../com.aspose.words/specialchar)
```
public class FormField extends SpecialChar
```

Представляет одно поле формы.

 Чтобы узнать больше, посетите**Working with Form Fields** документальная статья.

Microsoft Word предоставляет следующие поля формы: флажок, ввод текста и раскрывающийся список (поле со списком).

**FormField** является встроенным узлом и может быть только потомком**Paragraph**.

**FormField** представлен в документе специальным символом и расположен как символ в строке текста.

Полное поле формы в документе Word представляет собой сложную структуру, представленную несколькими узлами: начало поля, код поля, такой как FORMTEXT, данные поля формы, разделитель полей, результат поля, конец поля и закладка. Чтобы программно создать поля формы в документе Word, используйте[DocumentBuilder.insertCheckBox(java.lang.String, boolean, int)](../../com.aspose.words/documentbuilder\#insertCheckBox-java.lang.String--boolean--int-), **M:Aspose.Words.DocumentBuilder.InsertTextInput(System.String,Aspose.Words.Fields.TextFormFieldType,System.String,System.String,System.Int32)** а также[DocumentBuilder.insertComboBox(java.lang.String, java.lang.String[], int)](../../com.aspose.words/documentbuilder\#insertComboBox-java.lang.String--java.lang.String----int-) которые гарантируют, что все узлы поля формы созданы в правильном порядке и в подходящем состоянии.
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Принимает посетителя. |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Создает дубликат узла. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Получает первого предка указанного типа объекта. |
| [getCalculateOnExit()](#getCalculateOnExit--) | Истинно, если ссылки на указанное поле формы автоматически обновляются при выходе из поля. |
| [getCheckBoxSize()](#getCheckBoxSize--) | Получает размер флажка в пунктах. |
| [getChecked()](#getChecked--) | Получает проверенный статус поля формы флажка. |
| [getClass()](#getClass--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Задает идентификатор пользовательского узла. |
| [getDefault()](#getDefault--) | Получает значение по умолчанию для поля формы флажка. |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | Получает документ, которому принадлежит этот узел. |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getDropDownItems()](#getDropDownItems--) | Предоставляет доступ к элементам раскрывающегося поля формы. |
| [getDropDownSelectedIndex()](#getDropDownSelectedIndex--) | Получает индекс, указывающий текущий выбранный элемент в поле раскрывающейся формы. |
| [getEnabled()](#getEnabled--) | Истинно, если поле формы включено. |
| [getEntryMacro()](#getEntryMacro--) | Получает имя макроса записи для поля формы. |
| [getExitMacro()](#getExitMacro--) | Получает имя макроса выхода для поля формы. |
| [getFont()](#getFont--) | Предоставляет доступ к форматированию шрифта этого объекта. |
| [getHelpText()](#getHelpText--) | Получает текст, отображаемый в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает клавишу F1. |
| [getMaxLength()](#getMaxLength--) | Максимальная длина текстового поля. |
| [getName()](#getName--) | Получает имя поля формы. |
| [getNextSibling()](#getNextSibling--) | Получает узел, следующий сразу за этим узлом. |
| [getNodeType()](#getNodeType--) |  Возвращает**NodeType.FormField**. |
| [getOwnHelp()](#getOwnHelp--) | Указывает источник текста, отображаемого в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает клавишу F1. |
| [getOwnStatus()](#getOwnStatus--) | Указывает источник текста, который отображается в строке состояния, когда поле формы находится в фокусе. |
| [getParentNode()](#getParentNode--) | Получает непосредственного родителя этого узла. |
| [getParentParagraph()](#getParentParagraph--) |  Извлекает родителя[Paragraph](../../com.aspose.words/paragraph) этого узла. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange--) |  Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле. |
| [getResult()](#getResult--) | Получает строку, представляющую результат этого поля формы. |
| [getStatusText()](#getStatusText--) | Получает текст, отображаемый в строке состояния, когда поле формы имеет фокус. |
| [getText()](#getText--) | Получает специальный символ, который представляет этот узел. |
| [getTextInputDefault()](#getTextInputDefault--) | Получает строку по умолчанию или выражение вычисления поля текстовой формы. |
| [getTextInputFormat()](#getTextInputFormat--) | Получает форматирование текста для поля текстовой формы. |
| [getTextInputType()](#getTextInputType--) | Получает тип поля текстовой формы. |
| [getType()](#getType--) | Возвращает тип поля формы. |
| [hashCode()](#hashCode--) |  |
| [isCheckBoxExactSize()](#isCheckBoxExactSize--) | Получает логическое значение, указывающее, является ли размер текстового поля автоматическим или заданным явно. |
| [isCheckBoxExactSize(boolean value)](#isCheckBoxExactSize-boolean-) | Задает логическое значение, указывающее, является ли размер текстового поля автоматическим или заданным явно. |
| [isComposite()](#isComposite--) | Возвращает true, если этот узел может содержать другие узлы. |
| [isDeleteRevision()](#isDeleteRevision--) | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [isFormatRevision()](#isFormatRevision--) | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [isInsertRevision()](#isInsertRevision--) | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [isMoveFromRevision()](#isMoveFromRevision--) |  Возвращает**true** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [isMoveToRevision()](#isMoveToRevision--) |  Возвращает**true** если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [remove()](#remove--) | Удаляет себя из родителя. |
| [removeField()](#removeField--) | Удаляет все поле формы, а не только специальный символ поля формы. |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setCalculateOnExit(boolean value)](#setCalculateOnExit-boolean-) | Истинно, если ссылки на указанное поле формы автоматически обновляются при выходе из поля. |
| [setCheckBoxSize(double value)](#setCheckBoxSize-double-) | Устанавливает размер флажка в пунктах. |
| [setChecked(boolean value)](#setChecked-boolean-) | Устанавливает проверенный статус поля формы флажка. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Задает идентификатор пользовательского узла. |
| [setDefault(boolean value)](#setDefault-boolean-) | Задает значение по умолчанию для поля формы флажка. |
| [setDropDownSelectedIndex(int value)](#setDropDownSelectedIndex-int-) | Задает индекс, указывающий текущий выбранный элемент в поле раскрывающейся формы. |
| [setEnabled(boolean value)](#setEnabled-boolean-) | Истинно, если поле формы включено. |
| [setEntryMacro(String value)](#setEntryMacro-java.lang.String-) | Задает имя макроса записи для поля формы. |
| [setExitMacro(String value)](#setExitMacro-java.lang.String-) | Задает имя макроса выхода для поля формы. |
| [setHelpText(String value)](#setHelpText-java.lang.String-) | Задает текст, отображаемый в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает клавишу F1. |
| [setMaxLength(int value)](#setMaxLength-int-) | Максимальная длина текстового поля. |
| [setName(String value)](#setName-java.lang.String-) | Задает имя поля формы. |
| [setOwnHelp(boolean value)](#setOwnHelp-boolean-) | Указывает источник текста, отображаемого в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает клавишу F1. |
| [setOwnStatus(boolean value)](#setOwnStatus-boolean-) | Указывает источник текста, который отображается в строке состояния, когда поле формы находится в фокусе. |
| [setResult(String value)](#setResult-java.lang.String-) | Задает строку, представляющую результат этого поля формы. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setStatusText(String value)](#setStatusText-java.lang.String-) | Задает текст, отображаемый в строке состояния, когда поле формы находится в фокусе. |
| [setTextInputDefault(String value)](#setTextInputDefault-java.lang.String-) | Задает строку по умолчанию или выражение вычисления поля текстовой формы. |
| [setTextInputFormat(String value)](#setTextInputFormat-java.lang.String-) | Задает форматирование текста для поля текстовой формы. |
| [setTextInputType(int value)](#setTextInputType-int-) | Задает тип поля текстовой формы. |
| [setTextInputValue(Object newValue)](#setTextInputValue-java.lang.Object-) |  Применяет формат текста, указанный в[getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-) и сохраняет значение в[getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-). |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Принимает посетителя.

Вызывает DocumentVisitor.VisitFormField.

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | Посетитель, который посетит узел. |

**Возвращает:**
boolean — False, если посетитель запросил остановку перечисления.
### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### dd() {#dd--}
```
public void dd()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean-}
```
public Node deepClone(boolean isCloneChildren)
```


Создает дубликат узла.

Этот метод служит конструктором копирования для узлов. Клонированный узел не имеет родителя, но принадлежит к тому же документу, что и исходный узел.

 Этот метод всегда выполняет глубокую копию узла.*isCloneChildren* Параметр указывает, следует ли также выполнять копирование всех дочерних узлов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| isCloneChildren | boolean | Значение true, чтобы рекурсивно клонировать поддерево в указанном узле; false, чтобы клонировать только сам узел. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Клонированный узел.
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontAttr | int |  |

**Возвращает:**
java.lang.Объект
### getAncestor(int ancestorType) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestorType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ancestorType | int |  |

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class-}
```
public CompositeNode getAncestor(Class ancestorType)
```


Получает первого предка указанного типа объекта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ancestorType | java.lang.Class | Тип объекта-предка для извлечения. |

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode) - предок указанного типа или ноль, если предок этого типа не найден.

Тип предка совпадает, если он равен ancestorType или является производным от ancestorType.
### getCalculateOnExit() {#getCalculateOnExit--}
```
public boolean getCalculateOnExit()
```


Истинно, если ссылки на указанное поле формы автоматически обновляются при выходе из поля.

 Параметр**CalculateOnExit** влияет только на поведение поля формы при открытии документа в Microsoft Word. Aspose.Words никогда не обновляет ссылки на поле формы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getCheckBoxSize() {#getCheckBoxSize--}
```
public double getCheckBoxSize()
```


 Получает размер флажка в пунктах. Имеет эффект только тогда, когда[isCheckBoxExactSize()](../../com.aspose.words/formfield\#isCheckBoxExactSize--) / [isCheckBoxExactSize(boolean)](../../com.aspose.words/formfield\#isCheckBoxExactSize-boolean-) правда.

Применимо только к полю формы флажка.

**Возвращает:**
double - Размер флажка в пунктах.
### getChecked() {#getChecked--}
```
public boolean getChecked()
```


 Получает проверенный статус поля формы флажка. Значение по умолчанию для этого свойства**false**.

Применимо только к полю формы флажка.

**Возвращает:**
boolean - проверенный статус поля формы флажка.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


Задает идентификатор пользовательского узла.

По умолчанию ноль.

Этот идентификатор можно установить и использовать произвольно. Например, как ключ для получения внешних данных.

Важное примечание: указанное значение не сохраняется в выходной файл и существует только в течение срока службы узла.

**Возвращает:**
int - соответствующее значение int.
### getDefault() {#getDefault--}
```
public boolean getDefault()
```


 Получает значение по умолчанию для поля формы флажка. Значение по умолчанию для этого свойства**false**.

Применимо только к полю формы флажка.

**Возвращает:**
boolean — значение по умолчанию для поля формы флажка.
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontAttr | int |  |

**Возвращает:**
java.lang.Объект
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Получает документ, которому принадлежит этот узел.

Узел всегда принадлежит документу, даже если он только что создан и еще не добавлен в дерево или удален из дерева.

**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase) - Документ, которому принадлежит этот узел.
### getDocument_IInline() {#getDocument-IInline--}
```
public DocumentBase getDocument_IInline()
```




**Возвращает:**
[DocumentBase](../../com.aspose.words/documentbase)
### getDropDownItems() {#getDropDownItems--}
```
public DropDownItemCollection getDropDownItems()
```


Предоставляет доступ к элементам раскрывающегося поля формы.

Microsoft Word допускает не более 25 элементов в раскрывающемся поле формы.

**Возвращает:**
[DropDownItemCollection](../../com.aspose.words/dropdownitemcollection) - соответствующий[DropDownItemCollection](../../com.aspose.words/dropdownitemcollection) ценность.
### getDropDownSelectedIndex() {#getDropDownSelectedIndex--}
```
public int getDropDownSelectedIndex()
```


Получает индекс, указывающий текущий выбранный элемент в поле раскрывающейся формы.

**Возвращает:**
int - индекс, указывающий текущий выбранный элемент в поле выпадающей формы.
### getEnabled() {#getEnabled--}
```
public boolean getEnabled()
```


Истинно, если поле формы включено.

Если поле формы включено, его содержимое может быть изменено по мере заполнения формы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getEntryMacro() {#getEntryMacro--}
```
public String getEntryMacro()
```


Получает имя макроса записи для поля формы.

Макрос ввода запускается, когда поле формы получает фокус в Microsoft Word.

Microsoft Word позволяет использовать строки длиной не более 32 символов.

**Возвращает:**
java.lang.String — Имя макроса записи для поля формы.
### getExitMacro() {#getExitMacro--}
```
public String getExitMacro()
```


Получает имя макроса выхода для поля формы.

Макрос выхода запускается, когда поле формы теряет фокус в Microsoft Word.

Microsoft Word позволяет использовать строки длиной не более 32 символов.

**Возвращает:**
java.lang.String — имя макроса выхода для поля формы.
### getFont() {#getFont--}
```
public Font getFont()
```


Предоставляет доступ к форматированию шрифта этого объекта.

**Возвращает:**
[Font](../../com.aspose.words/font) - соответствующий[Font](../../com.aspose.words/font) ценность.
### getHelpText() {#getHelpText--}
```
public String getHelpText()
```


Получает текст, отображаемый в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает клавишу F1.

Если для свойства OwnHelp установлено значение True, HelpText указывает значение текстовой строки. Если для параметра OwnHelp задано значение False, HelpText указывает имя записи автотекста, которая содержит текст справки для поля формы.

Microsoft Word позволяет использовать строки длиной не более 255 символов.

**Возвращает:**
java.lang.String — текст, отображаемый в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает F1.
### getMaxLength() {#getMaxLength--}
```
public int getMaxLength()
```


Максимальная длина текстового поля. Ноль, когда длина не ограничена.

**Возвращает:**
int - соответствующее значение int.
### getName() {#getName--}
```
public String getName()
```


Получает имя поля формы. Microsoft Word позволяет использовать строки длиной не более 20 символов.

**Возвращает:**
java.lang.String — имя поля формы.
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


Получает узел, следующий сразу за этим узлом. Если следующего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Узел, непосредственно следующий за этим узлом.
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


 Возвращает**NodeType.FormField**.

**Возвращает:**
 инт -**NodeType.FormField** . Возвращаемое значение является одним из[NodeType](../../com.aspose.words/nodetype) константы.
### getOwnHelp() {#getOwnHelp--}
```
public boolean getOwnHelp()
```


Указывает источник текста, отображаемого в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает клавишу F1.

Если True, отображается текст, заданный свойством HelpText. Если задано значение False, отображается текст в записи автотекста, заданный свойством HelpText.

**Возвращает:**
boolean - соответствующее логическое значение.
### getOwnStatus() {#getOwnStatus--}
```
public boolean getOwnStatus()
```


Указывает источник текста, который отображается в строке состояния, когда поле формы находится в фокусе.

Если true, отображается текст, заданный свойством StatusText. Если установлено значение false, отображается текст записи автотекста, заданный свойством StatusText.

**Возвращает:**
boolean - соответствующее логическое значение.
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Получает непосредственного родителя этого узла.

Если узел был только что создан и еще не добавлен в дерево, или если он был удален из дерева, родитель имеет значение null.

**Возвращает:**
[CompositeNode](../../com.aspose.words/compositenode) - Непосредственный родитель этого узла.
### getParentParagraph() {#getParentParagraph--}
```
public Paragraph getParentParagraph()
```


 Извлекает родителя[Paragraph](../../com.aspose.words/paragraph) этого узла.

**Возвращает:**
[Paragraph](../../com.aspose.words/paragraph) - соответствующий[Paragraph](../../com.aspose.words/paragraph) ценность.
### getParentParagraph_IInline() {#getParentParagraph-IInline--}
```
public Paragraph getParentParagraph_IInline()
```




**Возвращает:**
[Paragraph](../../com.aspose.words/paragraph)
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


Получает узел, непосредственно предшествующий этому узлу. Если предыдущего узла нет, возвращается нуль.

**Возвращает:**
[Node](../../com.aspose.words/node) - Узел, непосредственно предшествующий этому узлу.
### getRange() {#getRange--}
```
public Range getRange()
```


 Возвращает**Range** объект, который представляет часть документа, содержащегося в этом узле.

**Возвращает:**
[Range](../../com.aspose.words/range) - А**Range** объект, который представляет часть документа, содержащегося в этом узле.
### getResult() {#getResult--}
```
public String getResult()
```


Получает строку, представляющую результат этого поля формы.

Для поля текстовой формы результатом является текст, который находится в поле.

Для поля формы флажка результат может быть «1» или «0», чтобы указать, отмечен или не отмечен.

Для раскрывающегося поля формы результатом является строка, выбранная в раскрывающемся списке.

 Параметр[getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-) для поля текстовой формы не применяется текстовый формат, указанный в[getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-) . Если вы хотите установить значение и применить формат, используйте[setTextInputValue(java.lang.Object)](../../com.aspose.words/formfield\#setTextInputValue-java.lang.Object-) метод.

 Для поля текстовой формы[getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-) значение применяется, если значение равно null .

**Возвращает:**
java.lang.String — строка, представляющая результат этого поля формы.
### getStatusText() {#getStatusText--}
```
public String getStatusText()
```


Получает текст, отображаемый в строке состояния, когда поле формы имеет фокус.

Если для свойства OwnStatus установлено значение true, свойство StatusText определяет текст строки состояния. Если для свойства OwnStatus задано значение false, свойство StatusText указывает имя записи автотекста, которая содержит текст строки состояния для поля формы.

Microsoft Word позволяет использовать строки длиной не более 138 символов.

**Возвращает:**
java.lang.String — текст, отображаемый в строке состояния, когда поле формы находится в фокусе.
### getText() {#getText--}
```
public String getText()
```


Получает специальный символ, который представляет этот узел.

**Возвращает:**
java.lang.String — строка, содержащая символ, который представляет этот узел.
### getTextInputDefault() {#getTextInputDefault--}
```
public String getTextInputDefault()
```


Получает строку по умолчанию или выражение вычисления поля текстовой формы.

 Смысл этого свойства зависит от значения[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) имущество.

 Когда[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) является[TextFormFieldType.REGULAR](../../com.aspose.words/textformfieldtype\#REGULAR) или же[TextFormFieldType.NUMBER](../../com.aspose.words/textformfieldtype\#NUMBER), эта строка указывает строку по умолчанию для поля текстовой формы. Эта строка представляет собой содержимое, которое Microsoft Word будет отображать в документе, когда поле формы пусто.

 Когда[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) является[TextFormFieldType.CALCULATED](../../com.aspose.words/textformfieldtype\#CALCULATED), то эта строка содержит вычисляемое выражение. Выражение должно быть формулой, допустимой в соответствии с требованиями поля формулы Microsoft Word. Когда вы устанавливаете новое выражение с помощью этого свойства, Aspose.Words автоматически вычисляет результат формулы и вставляет его в поле формы.

Microsoft Word позволяет использовать строки длиной не более 255 символов.

**Возвращает:**
java.lang.String — строка по умолчанию или расчетное выражение поля текстовой формы.
### getTextInputFormat() {#getTextInputFormat--}
```
public String getTextInputFormat()
```


Получает форматирование текста для поля текстовой формы.

Если поле текстовой формы содержит обычный текст, допустимыми строками формата являются "", "ВЕРХНИЙ РЕГИСТР", "НИЖНИЙ РЕГИСТР", "ПЕРВАЯ ЗАГЛАВНАЯ" и "ЗАГЛАВНЫЙ РЕГИСТР". Строки нечувствительны к регистру.

Если поле текстовой формы содержит число или значение даты/времени, допустимыми строками формата являются числа или строки формата даты и времени.

Microsoft Word позволяет использовать строки длиной не более 64 символов.

**Возвращает:**
java.lang.String — Форматирование текста для поля текстовой формы.
### getTextInputType() {#getTextInputType--}
```
public int getTextInputType()
```


Получает тип поля текстовой формы.

**Возвращает:**
 int - Тип поля текстовой формы. Возвращаемое значение является одним из[TextFormFieldType](../../com.aspose.words/textformfieldtype) константы.
### getType() {#getType--}
```
public int getType()
```


Возвращает тип поля формы.

**Возвращает:**
 int - Тип поля формы. Возвращаемое значение является одним из[FieldType](../../com.aspose.words/fieldtype) константы.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isCheckBoxExactSize() {#isCheckBoxExactSize--}
```
public boolean isCheckBoxExactSize()
```


Получает логическое значение, указывающее, является ли размер текстового поля автоматическим или заданным явно.

Применимо только к полю формы флажка.

**Возвращает:**
boolean — логическое значение, указывающее, является ли размер текстового поля автоматическим или заданным явно.
### isCheckBoxExactSize(boolean value) {#isCheckBoxExactSize-boolean-}
```
public void isCheckBoxExactSize(boolean value)
```


Задает логическое значение, указывающее, является ли размер текстового поля автоматическим или заданным явно.

Применимо только к полю формы флажка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, является ли размер текстового поля автоматическим или заданным явно. |

### isComposite() {#isComposite--}
```
public boolean isComposite()
```


Возвращает true, если этот узел может содержать другие узлы. (31110,6)

**Возвращает:**
boolean — Истинно, если этот узел может содержать другие узлы.
### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
boolean — Истинно, если этот объект был удален в Microsoft Word при включенном отслеживании изменений.
### isFormatRevision() {#isFormatRevision--}
```
public boolean isFormatRevision()
```


Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
boolean — Истинно, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений.
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
boolean — True, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений.
### isMoveFromRevision() {#isMoveFromRevision--}
```
public boolean isMoveFromRevision()
```


 Возвращает**true** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
 логический -**true** если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений.
### isMoveToRevision() {#isMoveToRevision--}
```
public boolean isMoveToRevision()
```


 Возвращает**true** если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений.

**Возвращает:**
 логический -**true** если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | Верхний узел (предел) обхода. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Следующий узел в порядке предварительного заказа. Null, если достигнут rootNode.
### nodeTypeToString(int nodeType) {#nodeTypeToString-int-}
```
public static String nodeTypeToString(int nodeType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |

**Возвращает:**
java.lang.String
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | Верхний узел (предел) обхода. |

**Возвращает:**
[Node](../../com.aspose.words/node) - Предыдущий узел в порядке предварительного заказа. Null, если достигнут rootNode.
### remove() {#remove--}
```
public void remove()
```


Удаляет себя из родителя.

### removeField() {#removeField--}
```
public void removeField()
```


Удаляет все поле формы, а не только специальный символ поля формы. Если есть закладка, связанная с полем формы, закладка не удаляется.

### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

### setCalculateOnExit(boolean value) {#setCalculateOnExit-boolean-}
```
public void setCalculateOnExit(boolean value)
```


Истинно, если ссылки на указанное поле формы автоматически обновляются при выходе из поля.

 Параметр**CalculateOnExit** влияет только на поведение поля формы при открытии документа в Microsoft Word. Aspose.Words никогда не обновляет ссылки на поле формы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setCheckBoxSize(double value) {#setCheckBoxSize-double-}
```
public void setCheckBoxSize(double value)
```


 Устанавливает размер флажка в пунктах. Имеет эффект только тогда, когда[isCheckBoxExactSize()](../../com.aspose.words/formfield\#isCheckBoxExactSize--) / [isCheckBoxExactSize(boolean)](../../com.aspose.words/formfield\#isCheckBoxExactSize-boolean-) правда.

Применимо только к полю формы флажка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Размер флажка в пунктах. |

### setChecked(boolean value) {#setChecked-boolean-}
```
public void setChecked(boolean value)
```


 Устанавливает проверенный статус поля формы флажка. Значение по умолчанию для этого свойства**false**.

Применимо только к полю формы флажка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Отмеченный статус поля формы флажка. |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


Задает идентификатор пользовательского узла.

По умолчанию ноль.

Этот идентификатор можно установить и использовать произвольно. Например, как ключ для получения внешних данных.

Важное примечание: указанное значение не сохраняется в выходной файл и существует только в течение срока службы узла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setDefault(boolean value) {#setDefault-boolean-}
```
public void setDefault(boolean value)
```


 Задает значение по умолчанию для поля формы флажка. Значение по умолчанию для этого свойства**false**.

Применимо только к полю формы флажка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение по умолчанию поля формы флажка. |

### setDropDownSelectedIndex(int value) {#setDropDownSelectedIndex-int-}
```
public void setDropDownSelectedIndex(int value)
```


Задает индекс, указывающий текущий выбранный элемент в поле раскрывающейся формы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Индекс, указывающий текущий выбранный элемент в раскрывающемся поле формы. |

### setEnabled(boolean value) {#setEnabled-boolean-}
```
public void setEnabled(boolean value)
```


Истинно, если поле формы включено.

Если поле формы включено, его содержимое может быть изменено по мере заполнения формы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setEntryMacro(String value) {#setEntryMacro-java.lang.String-}
```
public void setEntryMacro(String value)
```


Задает имя макроса записи для поля формы.

Макрос ввода запускается, когда поле формы получает фокус в Microsoft Word.

Microsoft Word позволяет использовать строки длиной не более 32 символов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя макроса записи для поля формы. |

### setExitMacro(String value) {#setExitMacro-java.lang.String-}
```
public void setExitMacro(String value)
```


Задает имя макроса выхода для поля формы.

Макрос выхода запускается, когда поле формы теряет фокус в Microsoft Word.

Microsoft Word позволяет использовать строки длиной не более 32 символов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя макроса выхода для поля формы. |

### setHelpText(String value) {#setHelpText-java.lang.String-}
```
public void setHelpText(String value)
```


Задает текст, отображаемый в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает клавишу F1.

Если для свойства OwnHelp установлено значение True, HelpText указывает значение текстовой строки. Если для параметра OwnHelp задано значение False, HelpText указывает имя записи автотекста, которая содержит текст справки для поля формы.

Microsoft Word позволяет использовать строки длиной не более 255 символов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, отображаемый в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает клавишу F1. |

### setMaxLength(int value) {#setMaxLength-int-}
```
public void setMaxLength(int value)
```


Максимальная длина текстового поля. Ноль, когда длина не ограничена.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Задает имя поля формы. Microsoft Word позволяет использовать строки длиной не более 20 символов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя поля формы. |

### setOwnHelp(boolean value) {#setOwnHelp-boolean-}
```
public void setOwnHelp(boolean value)
```


Указывает источник текста, отображаемого в окне сообщения, когда поле формы находится в фокусе и пользователь нажимает клавишу F1.

Если True, отображается текст, заданный свойством HelpText. Если задано значение False, отображается текст в записи автотекста, заданный свойством HelpText.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setOwnStatus(boolean value) {#setOwnStatus-boolean-}
```
public void setOwnStatus(boolean value)
```


Указывает источник текста, который отображается в строке состояния, когда поле формы находится в фокусе.

Если true, отображается текст, заданный свойством StatusText. Если установлено значение false, отображается текст записи автотекста, заданный свойством StatusText.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Задает строку, представляющую результат этого поля формы.

Для поля текстовой формы результатом является текст, который находится в поле.

Для поля формы флажка результат может быть «1» или «0», чтобы указать, отмечен или не отмечен.

Для раскрывающегося поля формы результатом является строка, выбранная в раскрывающемся списке.

 Параметр[getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-) для поля текстовой формы не применяется текстовый формат, указанный в[getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-) . Если вы хотите установить значение и применить формат, используйте[setTextInputValue(java.lang.Object)](../../com.aspose.words/formfield\#setTextInputValue-java.lang.Object-) метод.

 Для поля текстовой формы[getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-) значение применяется, если значение равно null .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Строка, представляющая результат этого поля формы. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStatusText(String value) {#setStatusText-java.lang.String-}
```
public void setStatusText(String value)
```


Задает текст, отображаемый в строке состояния, когда поле формы находится в фокусе.

Если для свойства OwnStatus установлено значение true, свойство StatusText определяет текст строки состояния. Если для свойства OwnStatus задано значение false, свойство StatusText указывает имя записи автотекста, которая содержит текст строки состояния для поля формы.

Microsoft Word позволяет использовать строки длиной не более 138 символов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, отображаемый в строке состояния, когда поле формы находится в фокусе. |

### setTextInputDefault(String value) {#setTextInputDefault-java.lang.String-}
```
public void setTextInputDefault(String value)
```


Задает строку по умолчанию или выражение вычисления поля текстовой формы.

 Смысл этого свойства зависит от значения[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) имущество.

 Когда[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) является[TextFormFieldType.REGULAR](../../com.aspose.words/textformfieldtype\#REGULAR) или же[TextFormFieldType.NUMBER](../../com.aspose.words/textformfieldtype\#NUMBER), эта строка указывает строку по умолчанию для поля текстовой формы. Эта строка представляет собой содержимое, которое Microsoft Word будет отображать в документе, когда поле формы пусто.

 Когда[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-) является[TextFormFieldType.CALCULATED](../../com.aspose.words/textformfieldtype\#CALCULATED), то эта строка содержит вычисляемое выражение. Выражение должно быть формулой, допустимой в соответствии с требованиями поля формулы Microsoft Word. Когда вы устанавливаете новое выражение с помощью этого свойства, Aspose.Words автоматически вычисляет результат формулы и вставляет его в поле формы.

Microsoft Word позволяет использовать строки длиной не более 255 символов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Строка по умолчанию или расчетное выражение поля текстовой формы. |

### setTextInputFormat(String value) {#setTextInputFormat-java.lang.String-}
```
public void setTextInputFormat(String value)
```


Задает форматирование текста для поля текстовой формы.

Если поле текстовой формы содержит обычный текст, допустимыми строками формата являются "", "ВЕРХНИЙ РЕГИСТР", "НИЖНИЙ РЕГИСТР", "ПЕРВАЯ ЗАГЛАВНАЯ" и "ЗАГЛАВНЫЙ РЕГИСТР". Строки нечувствительны к регистру.

Если поле текстовой формы содержит число или значение даты/времени, допустимыми строками формата являются числа или строки формата даты и времени.

Microsoft Word позволяет использовать строки длиной не более 64 символов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Форматирование текста для поля текстовой формы. |

### setTextInputType(int value) {#setTextInputType-int-}
```
public void setTextInputType(int value)
```


Задает тип поля текстовой формы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Тип поля текстовой формы. Значение должно быть одним из[TextFormFieldType](../../com.aspose.words/textformfieldtype) константы. |

### setTextInputValue(Object newValue) {#setTextInputValue-java.lang.Object-}
```
public void setTextInputValue(Object newValue)
```


 Применяет формат текста, указанный в[getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-) и сохраняет значение в[getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| newValue | java.lang.Object |  Может быть строкой, числом или объектом DateTime.[getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-) value применяется, если newValue равно null . |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
```
public String toString(SaveOptions saveOptions)
```


Экспортирует содержимое узла в строку, используя указанные параметры сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Указывает параметры, управляющие способом сохранения узла. |

**Возвращает:**
java.lang.String — содержимое узла в указанном формате.
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
