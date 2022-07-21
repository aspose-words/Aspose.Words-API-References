---
title: Document
second_title: Справочник по API Aspose.Words для .NET
description: Представляет документ Word.
type: docs
weight: 420
url: /ru/net/aspose.words/document/
---
## Document class

Представляет документ Word.

```csharp
public class Document : DocumentBase
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Document](document#constructor)() | Создает пустой документ Word. |
| [Document](document#constructor_1)(Stream) | Открывает существующий документ из потока. Автоматически определяет формат файла. |
| [Document](document#constructor_3)(string) | Открывает существующий документ из файла. Автоматически определяет формат файла. |
| [Document](document#constructor_2)(Stream, LoadOptions) | Открывает существующий документ из потока. Позволяет указать дополнительные параметры, такие как пароль шифрования. |
| [Document](document#constructor_4)(string, LoadOptions) | Открывает существующий документ из файла. Позволяет указать дополнительные параметры, такие как пароль шифрования. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate) { get; set; } | Получает или задает полный путь к шаблону, прикрепленному к документу. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles) { get; set; } | Получает или задает флаг, указывающий, обновляются ли стили в документе в соответствии со стилями в прикрепленном шаблоне каждый раз, когда документ открывается в MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape) { get; set; } | Получает или задает форму фона документа. Может быть нулевым. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties) { get; } | Возвращает коллекцию, которая представляет все встроенные свойства документа. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Получает все непосредственные дочерние узлы этого узла. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions) { get; } | Предоставляет доступ к параметрам совместимости документов (то есть к настройкам пользователя, введенным на **Совместимость** вкладка **Опции** диалоговое окно в Word). |
| [Compliance](../../aspose.words/document/compliance) { get; } | Получает версию соответствия OOXML, определенную из содержимого загруженного документа. Имеет смысл только для документов OOXML. |
| [Count](../../aspose.words/compositenode/count) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties) { get; } | Возвращает коллекцию, которая представляет все настраиваемые свойства документа. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts) { get; set; } | Получает или задает набор пользовательских частей хранилища данных XML. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop) { get; set; } | Получает или задает интервал (в пунктах) между позициями табуляции по умолчанию. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures) { get; } | Получает коллекцию цифровых подписей для этого документа и результаты их проверки. |
| override [Document](../../aspose.words/documentbase/document) { get; } |  |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions) { get; } | Предоставляет параметры, управляющие нумерацией и расположением концевых сносок в этом документе. |
| [FieldOptions](../../aspose.words/document/fieldoptions) { get; } | Получает **FieldOptions**объект, представляющий параметры для управления обработкой полей в документе. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Получает первого потомка узла. |
| [FirstSection](../../aspose.words/document/firstsection) { get; } | Получает первый раздел в документе. |
| [FontInfos](../../aspose.words/documentbase/fontinfos) { get; } | Предоставляет доступ к свойствам шрифтов, используемых в этом документе. |
| [FontSettings](../../aspose.words/document/fontsettings) { get; set; } | Получает или задает параметры шрифта документа. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions) { get; } | Предоставляет параметры, управляющие нумерацией и расположением сносок в этом документе. |
| [Frameset](../../aspose.words/document/frameset) { get; } | Возвращает[`Frameset`](./frameset)instance, если этот документ представляет собой страницу фреймов. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument) { get; set; } | Получает или задает документ глоссария в этом документе или шаблоне. Глоссарий — это хранилище для записей автотекста, автозамены и стандартных блоков, определенных в документе. |
| [GrammarChecked](../../aspose.words/document/grammarchecked) { get; set; } | Возвращает **истинный** если документ проверен на грамматику. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| [HasMacros](../../aspose.words/document/hasmacros) { get; } | Возвращает **истинный** если документ имеет проект VBA (макросы). |
| [HasRevisions](../../aspose.words/document/hasrevisions) { get; } | Возвращает **истинный** есть ли в документе отслеживаемые изменения. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions) { get; } | Предоставляет доступ к параметрам переноса документа. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Получает последний дочерний элемент узла. |
| [LastSection](../../aspose.words/document/lastsection) { get; } | Получает последний раздел в документе. |
| [LayoutOptions](../../aspose.words/document/layoutoptions) { get; } | Получает **МакетОпции** объект, представляющий параметры для управления процессом компоновки этого документа. |
| [Lists](../../aspose.words/documentbase/lists) { get; } | Предоставляет доступ к форматированию списка, используемому в документе. |
| [MailMerge](../../aspose.words/document/mailmerge) { get; } | Возвращает **MailMerge** объект, представляющий функциональность слияния для документа. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings) { get; set; } | Получает или задает объект, содержащий всю информацию о слиянии для документа. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback) { get; set; } | Вызывается при вставке или удалении узла в документе. |
| override [NodeType](../../aspose.words/document/nodetype) { get; } | Возвращает **NodeType.Document** . |
| [OriginalFileName](../../aspose.words/document/originalfilename) { get; } | Получает исходное имя файла документа. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat) { get; } | Получает формат исходного документа, который был загружен в этот объект. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts) { get; set; } | Получает или задает набор настраиваемых частей (произвольное содержимое), которые связаны с пакетом OOXML с помощью «неизвестных связей». |
| [PageColor](../../aspose.words/documentbase/pagecolor) { get; set; } | Получает или задает цвет страницы документа. Это свойство является упрощенной версией[`BackgroundShape`](../documentbase/backgroundshape) . |
| [PageCount](../../aspose.words/document/pagecount) { get; } | Получает количество страниц в документе, рассчитанное самой последней операцией макета страницы. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [ProtectionType](../../aspose.words/document/protectiontype) { get; } | Получает текущий активный тип защиты документа. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation) { get; set; } | Получает или устанавливает флаг, указывающий, что Microsoft Word удалит всю информацию о пользователе из комментариев, редакций и свойств документа при сохранении документа. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback) { get; set; } | Позволяет контролировать загрузку внешних ресурсов. |
| [Revisions](../../aspose.words/document/revisions) { get; } | Получает коллекцию ревизий (отслеживаемых изменений), существующих в этом документе. |
| [RevisionsView](../../aspose.words/document/revisionsview) { get; set; } | Получает или задает значение, указывающее, следует ли работать с исходной или исправленной версией документа. |
| [Sections](../../aspose.words/document/sections) { get; } | Возвращает коллекцию, представляющую все разделы документа. |
| [ShadeFormData](../../aspose.words/document/shadeformdata) { get; set; } | Указывает, следует ли включать серое затенение полей формы. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors) { get; set; } | Указывает, отображать ли грамматические ошибки в этом документе. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors) { get; set; } | Указывает, отображать ли орфографические ошибки в этом документе. |
| [SpellingChecked](../../aspose.words/document/spellingchecked) { get; set; } | Возвращает **истинный** если документ проверен на орфографию. |
| [Styles](../../aspose.words/documentbase/styles) { get; } | Возвращает набор стилей, определенных в документе. |
| [Theme](../../aspose.words/document/theme) { get; } | Получает[`Theme`](./theme) объект для этого документа. |
| [TrackRevisions](../../aspose.words/document/trackrevisions) { get; set; } | **Истинный** если изменения отслеживаются при редактировании этого документа в Microsoft Word. |
| [Variables](../../aspose.words/document/variables) { get; } | Возвращает набор переменных, добавленных в документ или шаблон. |
| [VbaProject](../../aspose.words/document/vbaproject) { get; set; } | Получает или задает[`VbaProject`](./vbaproject) . |
| [VersionsCount](../../aspose.words/document/versionscount) { get; } | Получает количество версий документа, сохраненных в документе DOC. |
| [ViewOptions](../../aspose.words/document/viewoptions) { get; } | Предоставляет параметры для управления отображением документа в Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback) { get; set; } | Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |
| [Watermark](../../aspose.words/document/watermark) { get; } | Предоставляет доступ к водяному знаку документа. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes) { get; } | Возвращает коллекцию, представляющую список надстроек области задач. |
| [WriteProtection](../../aspose.words/document/writeprotection) { get; } | Предоставляет доступ к параметрам защиты документа от записи. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/document/accept)(DocumentVisitor) | Принимает посетителя. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions)() | Принимает все отслеживаемые изменения в документе. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [AppendDocument](../../aspose.words/document/appenddocument#appenddocument)(Document, ImportFormatMode) | Добавляет указанный документ в конец этого документа. |
| [AppendDocument](../../aspose.words/document/appenddocument#appenddocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Добавляет указанный документ в конец этого документа. |
| [Cleanup](../../aspose.words/document/cleanup#cleanup)() | Удаляет неиспользуемые стили и списки из документа. |
| [Cleanup](../../aspose.words/document/cleanup#cleanup_1)(CleanupOptions) | Удаляет из документа неиспользуемые стили и списки в зависимости от заданного[`CleanupOptions`](../cleanupoptions) . |
| [Clone](../../aspose.words/document/clone#clone)() | Выполняет глубокую копию[`Document`](../document) . |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [Compare](../../aspose.words/document/compare#compare)(Document, string, DateTime) | Сравнивает этот документ с другим документом, внося изменения в виде количества редакций и форматирования.[`Revision`](../revision) . |
| [Compare](../../aspose.words/document/compare#compare_1)(Document, string, DateTime, CompareOptions) | Сравнивает этот документ с другим документом, внося изменения в виде количества редакций и форматирования.[`Revision`](../revision) . Позволяет указать параметры сравнения, используя[`CompareOptions`](../../aspose.words.comparing/compareoptions) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate#copystylesfromtemplate)(Document) | Копирует стили из указанного шаблона в документ. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate#copystylesfromtemplate_1)(string) | Копирует стили из указанного шаблона в документ. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Зарезервировано для системного использования. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum)() | Если документ не содержит разделов, создается один раздел с одним абзацем. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting)() | Преобразует форматирование, указанное в стилях таблиц, в прямое форматирование таблиц в документе. |
| [ExtractPages](../../aspose.words/document/extractpages)(int, int) | Возвращает[`Document`](../document) объект, представляющий указанный диапазон страниц. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| [GetPageInfo](../../aspose.words/document/getpageinfo)(int) | Получает размер страницы, ориентацию и другую информацию о странице, которая может быть полезна для печати или рендеринга. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Получает текст этого узла и всех его дочерних элементов. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool) | Импортирует узел из другого документа в текущий документ. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool, ImportFormatMode) | Импортирует узел из другого документа в текущий документ с возможностью управления форматированием. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting)() | Объединяет прогоны с одинаковым форматированием во всех абзацах документа. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes)() | Изменяет значения типа поля[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype) из[`FieldStart`](../../aspose.words.fields/fieldstart) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator) ,[`FieldEnd`](../../aspose.words.fields/fieldend) во всем документе, чтобы они соответствовали типам полей, содержащимся в кодах полей. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Print](../../aspose.words/document/print#print)() | Печать всего документа на принтере по умолчанию. |
| [Print](../../aspose.words/document/print#print_1)(PrinterSettings) | Печать документа в соответствии с заданными настройками принтера, с использованием стандартного (без пользовательского интерфейса) контроллера печати. |
| [Print](../../aspose.words/document/print#print_3)(string) | Печать всего документа на указанном принтере, с использованием стандартного (без пользовательского интерфейса) контроллера печати. |
| [Print](../../aspose.words/document/print#print_2)(PrinterSettings, string) | Печать документа в соответствии с указанными настройками принтера, с использованием стандартного (без пользовательского интерфейса) контроллера печати и имени документа. |
| [Protect](../../aspose.words/document/protect#protect)(ProtectionType) | Защищает документ от изменений без изменения существующего пароля или назначает случайный пароль. |
| [Protect](../../aspose.words/document/protect#protect_1)(ProtectionType, string) | Защищает документ от изменений и дополнительно устанавливает пароль защиты. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Удаляет указанный дочерний узел. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences)() | Удаляет ссылки на внешние XML-схемы из этого документа. |
| [RemoveMacros](../../aspose.words/document/removemacros)() | Удаляет все макросы (проект VBA), а также панели инструментов и настройки команд из документа. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag) узлы-потомки текущего узла. |
| [RenderToScale](../../aspose.words/document/rendertoscale)(int, Graphics, float, float, float) | Преобразует страницу документа вGraphics объект в указанном масштабе. |
| [RenderToSize](../../aspose.words/document/rendertosize)(int, Graphics, float, float, float, float) | Преобразует страницу документа вGraphics объект до указанного размера. |
| [Save](../../aspose.words/document/save#save_2)(string) | Сохраняет документ в файл. Автоматически определяет формат сохранения из расширения. |
| [Save](../../aspose.words/document/save#save)(Stream, SaveFormat) | Сохраняет документ в поток, используя указанный формат. |
| [Save](../../aspose.words/document/save#save_1)(Stream, SaveOptions) | Сохраняет документ в поток, используя указанные параметры сохранения. |
| [Save](../../aspose.words/document/save#save_3)(string, SaveFormat) | Сохраняет документ в файл в указанном формате. |
| [Save](../../aspose.words/document/save#save_4)(string, SaveOptions) | Сохраняет документ в файл, используя указанные параметры сохранения. |
| [Save](../../aspose.words/document/save#save_5)(HttpResponse, string, ContentDisposition, SaveOptions) | Отправляет документ в браузер клиента. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions#starttrackrevisions)(string) | Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения версии. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions#starttrackrevisions_1)(string, DateTime) | Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения версии. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions)() | Останавливает автоматическую маркировку изменений документа как редакций. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [UnlinkFields](../../aspose.words/document/unlinkfields)() | Разъединяет поля во всем документе. |
| [Unprotect](../../aspose.words/document/unprotect#unprotect_1)() | Снимает защиту с документа независимо от пароля. |
| [Unprotect](../../aspose.words/document/unprotect#unprotect)(string) | Снимает защиту с документа, если указан правильный пароль. |
| [UpdateFields](../../aspose.words/document/updatefields)() | Обновляет значения полей во всем документе. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels)() | Обновляет метки списка для всех элементов списка в документе. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout)() | Перестраивает макет страницы документа. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail#updatethumbnail)() | Обновления[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail) документа с параметрами по умолчанию. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail#updatethumbnail_1)(ThumbnailGeneratingOptions) | Обновления[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail) документа по заданным параметрам. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount#updatewordcount)() | Обновляет свойства количества слов в документе. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount#updatewordcount_1)(bool) | Обновляет свойства количества слов в документе, опционально обновляет[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines) свойство. |

### Примечания

**Документ** является центральным объектом в библиотеке Aspose.Words.

Чтобы загрузить существующий документ в любой из[`LoadFormat`](../loadformat) форматы, передайте имя файла или поток в один из **Документ** конструкторы. Чтобы создать пустой документ, вызовите конструктор без параметров.

Используйте одну из перегрузок метода Save, чтобы сохранить документ в любом из каталогов .[`SaveFormat`](../saveformat) форматы.

Чтобы рисовать страницы документа непосредственно на **Графика** объект use [`RenderToScale`](./rendertoscale) или же[`RenderToSize`](./rendertosize) метод.

Для печати документа используйте один из[`Print`](./print)методы.

[`MailMerge`](./mailmerge) — это механизм отчетов Aspose.Words, который позволяет быстро и легко заполнять отчеты, разработанные в Microsoft Word, данными из различных источников данных. Данные могут быть из DataSet, DataTable, DataView, IDataReader или массива значений.  **MailMerge** будет просматривать записи, найденные в источнике данных, и вставлять их в поля слияния почты в документе, увеличивая его по мере необходимости.

**Документ** хранит информацию по всему документу, такую как[`Styles`](../documentbase/styles) , [`BuiltInDocumentProperties`](./builtindocumentproperties) ,[`CustomDocumentProperties`](./customdocumentproperties) , списки и макросы. Большинство этих объектов доступны через соответствующие свойства **Документ**.

**Документ**является корневым узлом дерева, которое содержит все остальные узлы документа. Дерево представляет собой шаблон проектирования Composite и во многом похож на XmlDocument. Содержимым документа можно свободно управлять программно:

* Доступ к узлам документа можно получить через типизированные коллекции, например[`Sections`](./sections) , [`ParagraphCollection`](../paragraphcollection) и т.п.
* Узлы документа могут быть выбраны по их типу узла с помощью [`GetChildNodes`](../compositenode/getchildnodes) или используя запрос XPath с[`SelectNodes`](../compositenode/selectnodes) или же[`SelectSingleNode`](../compositenode/selectsinglenode).
* Узлы содержимого могут быть добавлены или удалены из любого места документа с помощью [`InsertBefore`](../compositenode/insertbefore) ,[`InsertAfter`](../compositenode/insertafter) , [`RemoveChild`](../compositenode/removechild) и методы other , предоставляемые базовым классом[`CompositeNode`](../compositenode).
* Атрибуты форматирования каждого узла можно изменить с помощью свойств этого узла.

Рассмотрите возможность использования[`DocumentBuilder`](../documentbuilder) это упрощает задачу программного создания или заполнения дерева документов.

**Документ** может содержать только[`Section`](../section) объекты.

В Microsoft Word действительный документ должен иметь хотя бы один раздел.

### Примеры

Показывает, как выполнить слияние почты с данными из DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Ниже приведены два способа использования DataTable в качестве источника данных для слияния.
    // 1 — использовать всю таблицу для слияния, чтобы создать один выходной документ слияния для каждой строки в таблице:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Используйте одну строку таблицы для создания одного выходного документа слияния почты:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Создает исходный документ слияния.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Смотрите также

* class [DocumentBase](../documentbase)
* пространство имен [Aspose.Words](../../aspose.words)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
