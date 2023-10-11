---
title: Class Document
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Document сорт. Представляет документ Word.
type: docs
weight: 430
url: /ru/net/aspose.words/document/
---
## Document class

Представляет документ Word.

Чтобы узнать больше, посетите[Работа с документом](https://docs.aspose.com/words/net/working-with-document/) статья документации.

```csharp
public class Document : DocumentBase
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Document](document/#constructor)() | Создает пустой документ Word. |
| [Document](document/#constructor_1)(Stream) | Открывает существующий документ из потока. Автоматически определяет формат файла. |
| [Document](document/#constructor_3)(string) | Открывает существующий документ из файла. Автоматически определяет формат файла. |
| [Document](document/#constructor_2)(Stream, LoadOptions) | Открывает существующий документ из потока. Позволяет указать дополнительные параметры, такие как пароль шифрования. |
| [Document](document/#constructor_4)(string, LoadOptions) | Открывает существующий документ из файла. Позволяет указать дополнительные параметры, такие как пароль шифрования. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Получает или задает полный путь к шаблону, прикрепленному к документу. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Получает или задает флаг, указывающий, обновляются ли стили в документе в соответствии со стилями в прикрепленном шаблоне каждый раз, когда документ открывается в MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Получает или задает форму фона документа. Возможно`нулевой` . |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Возвращает коллекцию, которая представляет все встроенные свойства документа document. . |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Предоставляет доступ к параметрам совместимости документов (т. е. к пользовательским настройкам, введенным в **Совместимость** вкладка  **Параметры** диалог в Word). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | Получает версию соответствия OOXML, определенную на основе содержимого загруженного документа. Имеет смысл только для документов OOXML. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | Возвращает коллекцию, которая представляет все пользовательские свойства документа. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | Получает или задает коллекцию пользовательских частей хранилища XML-данных. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | Получает или задает интервал (в пунктах) между позициями табуляции по умолчанию. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | Получает коллекцию цифровых подписей для этого документа и результаты их проверки. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Получает этот экземпляр. |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | Предоставляет параметры, управляющие нумерацией и расположением сносок в этом документе. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | Получает[`FieldOptions`](../../aspose.words.fields/fieldoptions/) объект, который представляет параметры управления обработкой полей в документе. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого дочернего элемента узла. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | Получает первый раздел документа. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Предоставляет доступ к свойствам шрифтов, используемых в этом документе. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Получает или задает настройки шрифта документа. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Предоставляет параметры, управляющие нумерацией и расположением сносок в этом документе. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Возвращает[`Frameset`](./frameset/)экземпляр, если этот документ представляет собой страницу фреймов. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Получает или задает документ глоссария в этом документе или шаблоне. Документ глоссария — это хранилище для записей автотекста, автозамены и стандартных блоков, определенных в документе. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | Возвращает`истинный` если документ проверен на грамматику. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает`истинный` если у этого узла есть дочерние узлы. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | Возвращает`истинный` если в документе есть проект VBA (макросы). |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | Возвращает`истинный` если в документе есть отслеживаемые изменения. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Предоставляет доступ к параметрам расстановки переносов в документе. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | Указывает, включать ли текстовые поля, сноски и концевые сноски в статистику количества слов. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает`истинный` поскольку этот узел может иметь дочерние узлы. |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | Получает или задает настройку межсимвольного интервала в документе. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последнего дочернего узла узла. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | Получает последний раздел документа. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | Получает[`LayoutOptions`](../../aspose.words.layout/layoutoptions/) объект, представляющий параметры управления процессом макетирования этого документа. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Предоставляет доступ к форматированию списка, используемому в документе. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | Возвращает[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) объект, представляющий функцию слияния почты для документа. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | Получает или задает объект, содержащий всю информацию о слиянии почты для документа. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Вызывается, когда узел вставляется или удаляется в документе. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | ВозвращаетDocument . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | Получает исходное имя файла документа. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Получает формат исходного документа, который был загружен в этот объект. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | Получает или задает коллекцию пользовательских частей (произвольное содержимое), которые связаны с пакетом OOXML с помощью «неизвестных связей». |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Получает или задает цвет страницы документа. Это свойство представляет собой более простую версию[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | Получает количество страниц в документе, рассчитанное с помощью последней операции макета страницы. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Получает текущий активный тип защиты документа. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/) объект, представляющий часть документа, содержащуюся в этом узле. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Получает или задает флаг, указывающий, что Microsoft Word удалит всю пользовательскую информацию из комментариев, редакций и свойств документа при сохранении документа. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Позволяет контролировать загрузку внешних ресурсов. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Получает коллекцию редакций (отслеживаемых изменений), существующих в этом документе. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Получает или задает значение, указывающее, следует ли работать с исходной или исправленной версией документа. |
| [Sections](../../aspose.words/document/sections/) { get; } | Возвращает коллекцию, представляющую все разделы документа. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Указывает, включать ли затенение серым в полях формы. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Указывает, отображать ли грамматические ошибки в этом документе. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Указывает, отображать ли орфографические ошибки в этом документе. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | Возвращает`истинный` если документ проверен на орфографию. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Возвращает коллекцию стилей, определенных в документе. |
| [Theme](../../aspose.words/document/theme/) { get; } | Получает[`Theme`](./theme/) объект для этого документа. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | True, если изменения отслеживаются при редактировании этого документа в Microsoft Word. |
| [Variables](../../aspose.words/document/variables/) { get; } | Возвращает коллекцию переменных, добавленных в документ или шаблон. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Получает или устанавливает[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | Получает количество версий документа, хранящихся в документе DOC. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Предоставляет параметры для управления отображением документа в Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере данных или точности форматирования. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Обеспечивает доступ к водяному знаку документа. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Возвращает коллекцию, представляющую список надстроек области задач. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Предоставляет доступ к параметрам защиты документа от записи. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(DocumentVisitor) | Принимает посетителя. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Принимает все отслеживаемые изменения в документе. |
| override [AcceptEnd](../../aspose.words/document/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/document/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(Document, ImportFormatMode) | Добавляет указанный документ в конец этого документа. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Добавляет указанный документ в конец этого документа. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Удаляет неиспользуемые стили и списки из документа. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(CleanupOptions) | Удаляет из документа неиспользуемые стили и списки в зависимости от заданных[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | Выполняет глубокое копирование`Document` . |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [Compare](../../aspose.words/document/compare/#compare)(Document, string, DateTime) | Сравнивает этот документ с другим документом, внося изменения в зависимости от количества изменений формата и редактирования.[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(Document, string, DateTime, CompareOptions) | Сравнивает этот документ с другим документом, внося изменения в результате ряда изменений редактирования и формата.[`Revision`](../revision/) . Позволяет указать параметры сравнения, используя[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(Document) | Копирует стили из указанного шаблона в документ. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(string) | Копирует стили из указанного шаблона в документ. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | Если документ не содержит разделов, создается один раздел с одним абзацем. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Преобразует форматирование, указанное в стилях таблиц, в прямое форматирование таблиц в документе. |
| [ExtractPages](../../aspose.words/document/extractpages/)(int, int) | Возвращает`Document` объект, представляющий указанный диапазон страниц. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(int) | Получает размер страницы, ориентацию и другую информацию о странице, которая может быть полезна для печати или рендеринга. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних элементов. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool) | Импортирует узел из другого документа в текущий документ. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool, ImportFormatMode) | Импортирует узел из другого документа в текущий документ с возможностью управления форматированием. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | Объединяет прогоны с одинаковым форматированием во всех абзацах документа. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Изменяет значения типов полей.[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) из[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) во всем документе, чтобы они соответствовали типам полей, содержащимся в кодах полей. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [Print](../../aspose.words/document/print/#print)() | Печатает весь документ на принтере по умолчанию. |
| [Print](../../aspose.words/document/print/#print_1)(PrinterSettings) | Печатает документ в соответствии с указанными настройками принтера, с использованием стандартного (без пользовательского интерфейса) контроллера печати. |
| [Print](../../aspose.words/document/print/#print_3)(string) | Распечатайте весь документ на указанном принтере, , используя стандартный контроллер печати (без пользовательского интерфейса). |
| [Print](../../aspose.words/document/print/#print_2)(PrinterSettings, string) | Печатает документ в соответствии с указанными настройками принтера, с использованием стандартного контроллера печати (без пользовательского интерфейса) и имени документа. |
| [Protect](../../aspose.words/document/protect/#protect)(ProtectionType) | Защищает документ от изменений без изменения существующего пароля или назначает случайный пароль. |
| [Protect](../../aspose.words/document/protect/#protect_1)(ProtectionType, string) | Защищает документ от изменений и дополнительно устанавливает пароль защиты. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя от родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Удаляет внешние ссылки на схемы XML из этого документа. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Удаляет из документа все макросы (проект VBA), а также панели инструментов и настройки команд. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/)узлы-потомки текущего узла. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(int, Graphics, float, float, float) | Преобразует страницу документа вGraphics объект в указанном масштабе. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(int, Graphics, float, float, float, float) | Преобразует страницу документа вGraphics объект указанного размера. |
| [Save](../../aspose.words/document/save/#save_2)(string) | Сохраняет документ в файл. Автоматически определяет формат сохранения из расширения. |
| [Save](../../aspose.words/document/save/#save)(Stream, SaveFormat) | Сохраняет документ в поток, используя указанный формат. |
| [Save](../../aspose.words/document/save/#save_1)(Stream, SaveOptions) | Сохраняет документ в поток, используя указанные параметры сохранения. |
| [Save](../../aspose.words/document/save/#save_3)(string, SaveFormat) | Сохраняет документ в файл указанного формата. |
| [Save](../../aspose.words/document/save/#save_4)(string, SaveOptions) | Сохраняет документ в файл, используя указанные параметры сохранения. |
| [Save](../../aspose.words/document/save/#save_5)(HttpResponse, string, ContentDisposition, SaveOptions) | Отправляет документ в браузер клиента. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Выбирает первый[`Node`](../node/) которое соответствует выражению XPath. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(string) | Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения версии. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(string, DateTime) | Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения версии. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Останавливает автоматическую маркировку изменений документа как редакций. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Отменяет связь полей во всем документе. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Снимает защиту с документа независимо от пароля. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(string) | Снимает защиту с документа, если указан правильный пароль. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Обновляет значения полей во всем документе. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Обновляет метки списка для всех элементов списка в документе. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Перестраивает макет страницы документа. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Обновления[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) документа с использованием параметров по умолчанию. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(ThumbnailGeneratingOptions) | Обновления[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) документа согласно указанным параметрам. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Обновляет свойства количества слов в документе. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(bool) | Обновляет свойства количества слов в документе, при необходимости обновляет.[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) свойство. |

### Примечания

`Document` является центральным объектом в библиотеке Aspose.Words.

Чтобы загрузить существующий документ в любой из[`LoadFormat`](../loadformat/) форматы, передайте имя файла или поток в один из`Document`конструкторы. Чтобы создать пустой документ, вызовите конструктор the без параметров.

Используйте одну из перегрузок метода Save, чтобы сохранить документ в любом из [`SaveFormat`](../saveformat/) форматы.

Чтобы нарисовать страницы документа непосредственно на **Графика** объект use [`RenderToScale`](./rendertoscale/) или[`RenderToSize`](./rendertosize/) метод.

Чтобы распечатать документ, воспользуйтесь одним из[`Print`](./print/) методы.

[`MailMerge`](./mailmerge/) - это механизм отчетов Aspose.Words, который позволяет быстро и легко заполнять отчеты, созданные в Microsoft Word, данными из различных источников данных. Данные могут быть из DataSet, DataTable, DataView, IDataReader или массива значений.  **MailMerge** просматривает записи, найденные в источнике данных, и вставляет их в поля слияния почты в документе, увеличивая его по мере необходимости.

`Document` хранит информацию по всему документу, такую как[`Styles`](../documentbase/styles/) , [`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/) списки и макросы. Большинство этих объектов доступны через соответствующие свойства`Document`.

`Document` является корневым узлом дерева, которое содержит все остальные узлы документа. Дерево представляет собой составной шаблон проектирования и во многом похоже на XmlDocument. Содержимым документа можно свободно манипулировать программно:

* Доступ к узлам документа можно получить через типизированные коллекции, например[`Sections`](./sections/) , [`ParagraphCollection`](../paragraphcollection/) и т. д.
* Узлы документа можно выбрать по типу узла с помощью .[`GetChildNodes`](../compositenode/getchildnodes/) или используя запрос XPath с[`SelectNodes`](../compositenode/selectnodes/) или[`SelectSingleNode`](../compositenode/selectsinglenode/).
* Узлы контента можно добавлять или удалять из любого места документа с помощью .Node) ,Node) , Node) и другие методы, предоставляемые базовым классом[`CompositeNode`](../compositenode/).
* Атрибуты форматирования каждого узла можно изменить с помощью свойств этого узла.

Рассмотрите возможность использования[`DocumentBuilder`](../documentbuilder/)это упрощает задачу программного создания или заполнения дерева документа.

`Document` может содержать только[`Section`](../section/) объекты.

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

    // Ниже приведены два способа использования DataTable в качестве источника данных для слияния почты.
    // 1 — использовать всю таблицу для слияния почты, чтобы создать один выходной документ слияния почты для каждой строки в таблице:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 — использовать одну строку таблицы для создания одного выходного документа слияния почты:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Создает исходный документ слияния почты.
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

* class [DocumentBase](../documentbase/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


