---
title: com.aspose.words
second_title: Справочник по API Aspose.Words для Java
description: Пакет com.aspose.words предоставляет классы для создания, преобразования, изменения, рендеринга и печати документов Microsoft Word без использования Microsoft Word.
type: docs
weight: 10
url: /ru/java/com.aspose.words/
---


**com.aspose.words** пакет предоставляет классы для создания, преобразования, изменения, рендеринга и печати документов Microsoft Word без использования Microsoft Word.

Aspose.Words полностью написан на Java. Microsoft Word не требуется для использования Aspose.Words.

 Классы в**com.aspose.words**package заимствовал лучшие практики из двух известных фреймворков: Microsoft Word Automation и System.Xml. Документ в Aspose.Words представлен деревом узлов, как и в XML DOM. Там, где это возможно, имена классов, методов и свойств совпадают с именами в Microsoft Word Automation.

Основные классы в этом пространстве имен:

 *  **Document** — основной класс объектной модели, представляющий документ Microsoft Word.
 *  **DocumentBuilder** предоставляет простой способ вставки содержимого и форматирования в документ.
 *  **Node** является базовым классом для всех узлов в документе.
 *  **CompositeNode** является базовым классом для всех узлов документа, которые могут содержать другие узлы, например**Paragraph**, **Section** а также**Table** а также .

**com.aspose.words** Пакет также содержит классы, формирующие механизм создания отчетов Aspose.Words. Механизм создания отчетов позволяет быстро и легко заполнять документы, созданные в Microsoft Word, данными из различных источников данных, таких как**java.sql.ResultSet**, **array of ResultSets**, **com.aspose.words.net.System.Data.DataSet** или**array of values**.

**MailMerge** объект, обеспечивающий доступ к функциям отчетности, доступен через**Document.MailMerge** имущество.


## Классы

| Учебный класс | Описание |
| --- | --- |
| [AbsolutePositionTab](../com.aspose.words/absolutepositiontab) | Табуляция абсолютной позиции — это символ, который используется для перемещения позиции в текущей строке текста при отображении этого содержимого WordprocessingML. |
| [ArrowLength](../com.aspose.words/arrowlength) | Длина стрелки в конце строки. |
| [ArrowType](../com.aspose.words/arrowtype) | Указывает тип стрелки на конце строки. |
| [ArrowWidth](../com.aspose.words/arrowwidth) | Ширина стрелки в конце строки. |
| [AsposeWordsPrintDocument](../com.aspose.words/asposewordsprintdocument) |  Обеспечивает реализацию по умолчанию для печати[Document](../com.aspose.words/document) в среде печати Java. |
| [AutoFitBehavior](../com.aspose.words/autofitbehavior) |  Определяет, как Aspose.Words изменяет размер таблицы при вызове **M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)** метод. |
| [AxisBound](../com.aspose.words/axisbound) | Представляет минимальную или максимальную границу значений оси. |
| [AxisBuiltInUnit](../com.aspose.words/axisbuiltinunit) | Указывает единицы отображения для оси. |
| [AxisCategoryType](../com.aspose.words/axiscategorytype) | Определяет тип оси категорий. |
| [AxisCrosses](../com.aspose.words/axiscrosses) | Определяет возможные точки пересечения оси. |
| [AxisDisplayUnit](../com.aspose.words/axisdisplayunit) | Предоставляет доступ к параметрам масштабирования единиц отображения для оси значений. |
| [AxisScaleType](../com.aspose.words/axisscaletype) | Определяет возможные типы шкалы для оси. |
| [AxisScaling](../com.aspose.words/axisscaling) | Представляет параметры масштабирования оси. |
| [AxisTickLabelPosition](../com.aspose.words/axisticklabelposition) | Определяет возможные позиции для галочек. |
| [AxisTickMark](../com.aspose.words/axistickmark) | Определяет возможные позиции делений. |
| [AxisTimeUnit](../com.aspose.words/axistimeunit) | Определяет единицу времени для осей. |
| [BarcodeParameters](../com.aspose.words/barcodeparameters) | Класс-контейнер для параметров штрих-кода для передачи в BarcodeGenerator. |
| [BaseWebExtensionCollection](../com.aspose.words/basewebextensioncollection) |  Базовый класс для[TaskPaneCollection](../com.aspose.words/taskpanecollection), [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection), [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection) а также[WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection) коллекции. |
| [BasicTextShaperCache](../com.aspose.words/basictextshapercache) |  |
| [BlockImportMode](../com.aspose.words/blockimportmode) | Указывает, как свойства элементов уровня блока импортируются из документов на основе HTML. |
| [Body](../com.aspose.words/body) | Представляет контейнер для основного текста раздела. |
| [Bookmark](../com.aspose.words/bookmark) | Представляет одну закладку. |
| [BookmarkCollection](../com.aspose.words/bookmarkcollection) |  Коллекция[Bookmark](../com.aspose.words/bookmark) объекты, представляющие закладки в указанном диапазоне. |
| [BookmarkEnd](../com.aspose.words/bookmarkend) | Представляет конец закладки в документе Word. |
| [BookmarkStart](../com.aspose.words/bookmarkstart) | Представляет начало закладки в документе Word. |
| [BookmarksOutlineLevelCollection](../com.aspose.words/bookmarksoutlinelevelcollection) | Набор уровней контура отдельных закладок. |
| [Border](../com.aspose.words/border) | Представляет границу объекта. |
| [BorderCollection](../com.aspose.words/bordercollection) | Коллекция объектов Border. |
| [BorderType](../com.aspose.words/bordertype) | Определяет стороны границы. |
| [BreakType](../com.aspose.words/breaktype) | Задает тип разрыва внутри документа. |
| [BuildVersionInfo](../com.aspose.words/buildversioninfo) | Предоставляет информацию о текущем названии и версии продукта. |
| [BuildingBlock](../com.aspose.words/buildingblock) | Представляет запись документа глоссария, такую как стандартный блок, автотекст или запись автозамены. |
| [BuildingBlockBehavior](../com.aspose.words/buildingblockbehavior) | Определяет поведение, которое должно применяться к содержимому стандартного блока, когда он вставляется в основной документ. |
| [BuildingBlockCollection](../com.aspose.words/buildingblockcollection) |  Коллекция[BuildingBlock](../com.aspose.words/buildingblock) объекты в документе. |
| [BuildingBlockGallery](../com.aspose.words/buildingblockgallery) | Указывает предопределенную галерею, в которую классифицируется стандартный блок. |
| [BuildingBlockType](../com.aspose.words/buildingblocktype) | Задает тип стандартного блока. |
| [BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties) | Коллекция встроенных свойств документа. |
| [CalendarType](../com.aspose.words/calendartype) | Указывает тип календаря. |
| [Cell](../com.aspose.words/cell) | Представляет ячейку таблицы. |
| [CellCollection](../com.aspose.words/cellcollection) |  Предоставляет типизированный доступ к коллекции[Cell](../com.aspose.words/cell) узлы. |
| [CellFormat](../com.aspose.words/cellformat) | Представляет все форматирование для ячейки таблицы. |
| [CellMerge](../com.aspose.words/cellmerge) | Указывает, как ячейка в таблице объединяется с другими ячейками. |
| [CellVerticalAlignment](../com.aspose.words/cellverticalalignment) | Задает вертикальное выравнивание текста внутри ячейки таблицы. |
| [CertificateHolder](../com.aspose.words/certificateholder) |  Представляет собой держателя**X509Certificate2** пример. |
| [ChapterPageSeparator](../com.aspose.words/chapterpageseparator) | Определяет символ-разделитель, который появляется между главой и номером страницы. |
| [Chart](../com.aspose.words/chart) | Предоставляет доступ к свойствам формы диаграммы. |
| [ChartAxis](../com.aspose.words/chartaxis) | Представляет параметры оси диаграммы. |
| [ChartAxisType](../com.aspose.words/chartaxistype) | Указывает тип оси диаграммы. |
| [ChartDataLabel](../com.aspose.words/chartdatalabel) | Представляет метку данных в точке диаграммы или на линии тренда. |
| [ChartDataLabelCollection](../com.aspose.words/chartdatalabelcollection) |  Представляет собой совокупность[ChartDataLabel](../com.aspose.words/chartdatalabel). |
| [ChartDataPoint](../com.aspose.words/chartdatapoint) | Позволяет указать форматирование одной точки данных на диаграмме. |
| [ChartDataPointCollection](../com.aspose.words/chartdatapointcollection) |  Представляет собой коллекцию[ChartDataPoint](../com.aspose.words/chartdatapoint). |
| [ChartFormat](../com.aspose.words/chartformat) | Представляет форматирование элемента диаграммы. |
| [ChartLegend](../com.aspose.words/chartlegend) | Представляет свойства легенды диаграммы. |
| [ChartLegendEntry](../com.aspose.words/chartlegendentry) | Представляет запись легенды диаграммы. |
| [ChartLegendEntryCollection](../com.aspose.words/chartlegendentrycollection) | Представляет коллекцию записей легенды диаграммы. |
| [ChartMarker](../com.aspose.words/chartmarker) | Представляет маркер данных диаграммы. |
| [ChartNumberFormat](../com.aspose.words/chartnumberformat) | Представляет числовое форматирование родительского элемента. |
| [ChartSeries](../com.aspose.words/chartseries) | Представляет свойства ряда диаграммы. |
| [ChartSeriesCollection](../com.aspose.words/chartseriescollection) |  Представляет собой коллекцию[ChartSeries](../com.aspose.words/chartseries). |
| [ChartTitle](../com.aspose.words/charttitle) | Предоставляет доступ к свойствам заголовка диаграммы. |
| [ChartType](../com.aspose.words/charttype) | Определяет тип диаграммы. |
| [ChmLoadOptions](../com.aspose.words/chmloadoptions) |  Позволяет указать дополнительные параметры при загрузке документа CHM в[Document](../com.aspose.words/document) объект. |
| [CleanupOptions](../com.aspose.words/cleanupoptions) | Позволяет указать параметры очистки документа. |
| [Cluster](../com.aspose.words/cluster) |  |
| [ColorMode](../com.aspose.words/colormode) | Указывает, как отображаются цвета. |
| [Comment](../com.aspose.words/comment) | Представляет контейнер для текста комментария. |
| [CommentCollection](../com.aspose.words/commentcollection) |  Предоставляет типизированный доступ к коллекции[Comment](../com.aspose.words/comment) узлы. |
| [CommentDisplayMode](../com.aspose.words/commentdisplaymode) | Задает режим отображения комментариев к документу. |
| [CommentRangeEnd](../com.aspose.words/commentrangeend) | Обозначает конец области текста, с которой связан комментарий. |
| [CommentRangeStart](../com.aspose.words/commentrangestart) | Обозначает начало области текста, с которой связан комментарий. |
| [CompareOptions](../com.aspose.words/compareoptions) | Позволяет выбрать дополнительные параметры для операции сравнения документов. |
| [ComparisonEvaluationResult](../com.aspose.words/comparisonevaluationresult) | Результат сравнительной оценки. |
| [ComparisonExpression](../com.aspose.words/comparisonexpression) | Выражение сравнения. |
| [ComparisonTargetType](../com.aspose.words/comparisontargettype) | Позволяет указать базовый документ, который будет использоваться при сравнении. |
| [Compatibility](../com.aspose.words/compatibility) | Указывает имена параметров совместимости. |
| [CompatibilityOptions](../com.aspose.words/compatibilityoptions) |  Содержит параметры совместимости (то есть пользовательские настройки, введенные на**Compatibility** вкладка**Options** диалоговое окно в Microsoft Word). |
| [CompositeNode](../com.aspose.words/compositenode) | Базовый класс для узлов, которые могут содержать другие узлы. |
| [CompressionLevel](../com.aspose.words/compressionlevel) | Уровень сжатия для файлов OOXML. |
| [ConditionalStyle](../com.aspose.words/conditionalstyle) | Представляет специальное форматирование, примененное к некоторой области таблицы с назначенным стилем таблицы. |
| [ConditionalStyleCollection](../com.aspose.words/conditionalstylecollection) |  Представляет собой совокупность[ConditionalStyle](../com.aspose.words/conditionalstyle) объекты. |
| [ConditionalStyleType](../com.aspose.words/conditionalstyletype) | Представляет возможные области таблицы, для которых может быть определено условное форматирование в стиле таблицы. |
| [ContentDisposition](../com.aspose.words/contentdisposition) | Перечисляет различные способы представления документа в браузере клиента. |
| [ContinuousSectionRestart](../com.aspose.words/continuoussectionrestart) | Представляет различное поведение при вычислении номеров страниц в непрерывном разделе, который перезапускает нумерацию страниц. |
| [ControlChar](../com.aspose.words/controlchar) | Управляющие символы часто встречаются в документах. |
| [ConvertUtil](../com.aspose.words/convertutil) | Предоставляет вспомогательные функции для преобразования между различными единицами измерения. |
| [CssSavingArgs](../com.aspose.words/csssavingargs) |  Предоставляет данные для[ICssSavingCallback.\#cssSaving(com.aspose.words.CssSavingArgs)](../com.aspose.words/icsssavingcallback\#cssSaving-com.aspose.words.CssSavingArgs-) мероприятие. |
| [CssStyleSheetType](../com.aspose.words/cssstylesheettype) | Указывает, как стили CSS (каскадные таблицы стилей) экспортируются в HTML. |
| [CsvDataLoadOptions](../com.aspose.words/csvdataloadoptions) | Представляет параметры анализа данных CSV. |
| [CsvDataSource](../com.aspose.words/csvdatasource) | Предоставляет доступ к данным CSV-файла или потока для использования в отчете. |
| [CurrentThreadSettings](../com.aspose.words/currentthreadsettings) | Этот класс помогает установить локаль и часовой пояс, изолированные от потоков, для приложения Aspose.Words. |
| [CustomDocumentProperties](../com.aspose.words/customdocumentproperties) | Коллекция настраиваемых свойств документа. |
| [CustomPart](../com.aspose.words/custompart) | Представляет пользовательскую часть (произвольное содержимое), которая не определена стандартом ISO/IEC 29500. |
| [CustomPartCollection](../com.aspose.words/custompartcollection) |  Представляет собой совокупность[CustomPart](../com.aspose.words/custompart) объекты. |
| [CustomXmlPart](../com.aspose.words/customxmlpart) | Представляет часть хранилища пользовательских данных XML (пользовательские данные XML в пакете). |
| [CustomXmlPartCollection](../com.aspose.words/customxmlpartcollection) | Представляет коллекцию пользовательских XML-частей. |
| [CustomXmlProperty](../com.aspose.words/customxmlproperty) | Представляет один настраиваемый XML-атрибут или свойство смарт-тега. |
| [CustomXmlPropertyCollection](../com.aspose.words/customxmlpropertycollection) | Представляет набор настраиваемых XML-атрибутов или свойств смарт-тегов. |
| [CustomXmlSchemaCollection](../com.aspose.words/customxmlschemacollection) | Коллекция строк, представляющих схемы XML, связанные с настраиваемой частью XML. |
| [DashStyle](../com.aspose.words/dashstyle) | Стиль пунктирной линии. |
| [DefaultFontSubstitutionRule](../com.aspose.words/defaultfontsubstitutionrule) | Правило замены шрифта по умолчанию. |
| [DigitalSignature](../com.aspose.words/digitalsignature) | Представляет цифровую подпись на документе и результат ее проверки. |
| [DigitalSignatureCollection](../com.aspose.words/digitalsignaturecollection) | Предоставляет доступную только для чтения коллекцию цифровых подписей, прикрепленных к документу. |
| [DigitalSignatureType](../com.aspose.words/digitalsignaturetype) | Указывает тип цифровой подписи. |
| [DigitalSignatureUtil](../com.aspose.words/digitalsignatureutil) | Предоставляет методы для подписания документа. |
| [Direction](../com.aspose.words/direction) |  |
| [Dml3DEffectsRenderingMode](../com.aspose.words/dml3deffectsrenderingmode) | Указывает, как визуализируются эффекты 3D-формы. |
| [DmlEffectsRenderingMode](../com.aspose.words/dmleffectsrenderingmode) | Указывает, как эффекты DrawingML визуализируются для фиксированных форматов страниц. |
| [DmlRenderingMode](../com.aspose.words/dmlrenderingmode) | Указывает, как фигуры DrawingML отображаются в фиксированных форматах страниц. |
| [DocSaveOptions](../com.aspose.words/docsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#DOC](../com.aspose.words/saveformat\#DOC) или же[SaveFormat.\#DOT](../com.aspose.words/saveformat\#DOT) формат. |
| [Document](../com.aspose.words/document) | Представляет документ Word. |
| [DocumentBase](../com.aspose.words/documentbase) | Предоставляет абстрактный базовый класс для основного документа и глоссария документа Word. |
| [DocumentBuilder](../com.aspose.words/documentbuilder) | Предоставляет методы для вставки текста, изображений и другого содержимого, указания шрифта, форматирования абзаца и раздела. |
| [DocumentDirection](../com.aspose.words/documentdirection) | Позволяет указать направление потока текста в документе. |
| [DocumentLoadingArgs](../com.aspose.words/documentloadingargs) |  Аргумент, переданный в[IDocumentLoadingCallback.\#notify(com.aspose.words.DocumentLoadingArgs)](../com.aspose.words/idocumentloadingcallback\#notify-com.aspose.words.DocumentLoadingArgs-). |
| [DocumentPartSavingArgs](../com.aspose.words/documentpartsavingargs) |  Предоставляет данные для[IDocumentPartSavingCallback.\#documentPartSaving(com.aspose.words.DocumentPartSavingArgs)](../com.aspose.words/idocumentpartsavingcallback\#documentPartSaving-com.aspose.words.DocumentPartSavingArgs-) перезвонить. |
| [DocumentProperty](../com.aspose.words/documentproperty) | Представляет пользовательское или встроенное свойство документа. |
| [DocumentPropertyCollection](../com.aspose.words/documentpropertycollection) |  Базовый класс для[BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties) а также[CustomDocumentProperties](../com.aspose.words/customdocumentproperties) коллекции. |
| [DocumentReaderPluginLoadException](../com.aspose.words/documentreaderpluginloadexception) | Возникает во время загрузки документа, когда плагин, необходимый для чтения формата документа, не может быть загружен. |
| [DocumentSavingArgs](../com.aspose.words/documentsavingargs) |  Аргумент, переданный в[IDocumentSavingCallback.\#notify(com.aspose.words.DocumentSavingArgs)](../com.aspose.words/idocumentsavingcallback\#notify-com.aspose.words.DocumentSavingArgs-). |
| [DocumentSecurity](../com.aspose.words/documentsecurity) |  Используется как значение для[BuiltInDocumentProperties.\#getSecurity()](../com.aspose.words/builtindocumentproperties\#getSecurity--) / [BuiltInDocumentProperties.\#setSecurity(int)](../com.aspose.words/builtindocumentproperties\#setSecurity-int-) имущество. |
| [DocumentSplitCriteria](../com.aspose.words/documentsplitcriteria) |  Указывает, как документ разбивается на части при сохранении в[SaveFormat.\#HTML](../com.aspose.words/saveformat\#HTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat\#EPUB) или же[SaveFormat.\#AZW\_3](../com.aspose.words/saveformat\#AZW-3) формат. |
| [DocumentVisitor](../com.aspose.words/documentvisitor) | Базовый класс для пользовательских посетителей документов. |
| [DownsampleOptions](../com.aspose.words/downsampleoptions) | Позволяет указать параметры понижающей дискретизации. |
| [DropCapPosition](../com.aspose.words/dropcapposition) | Определяет позицию для текста буквицы. |
| [DropDownItemCollection](../com.aspose.words/dropdownitemcollection) | Набор строк, представляющих все элементы в раскрывающемся поле формы. |
| [EditableRange](../com.aspose.words/editablerange) | Представляет один редактируемый диапазон. |
| [EditableRangeEnd](../com.aspose.words/editablerangeend) | Представляет конец редактируемого диапазона в документе Word. |
| [EditableRangeStart](../com.aspose.words/editablerangestart) | Представляет начало редактируемого диапазона в документе Word. |
| [EditingLanguage](../com.aspose.words/editinglanguage) | Указывает язык редактирования. |
| [EditorType](../com.aspose.words/editortype) | Задает набор возможных псевдонимов (или групп редактирования), которые можно использовать в качестве псевдонимов, чтобы определить, разрешено ли текущему пользователю редактировать один диапазон, определенный редактируемым диапазоном в документе. |
| [EmbeddedFontFormat](../com.aspose.words/embeddedfontformat) |  Определяет формат конкретного встроенного шрифта внутри[FontInfo](../com.aspose.words/fontinfo) объект. |
| [EmbeddedFontStyle](../com.aspose.words/embeddedfontstyle) |  Определяет стиль встроенного шрифта внутри[FontInfo](../com.aspose.words/fontinfo) объект. |
| [EmfPlusDualRenderingMode](../com.aspose.words/emfplusdualrenderingmode) | Указывает, как Aspose.Words должен отображать метафайлы EMF+ Dual. |
| [EmphasisMark](../com.aspose.words/emphasismark) | Определяет возможные типы метки акцента. |
| [EndCap](../com.aspose.words/endcap) | Определяет стиль окончания строки. |
| [EndnoteOptions](../com.aspose.words/endnoteoptions) | Представляет параметры нумерации концевых сносок для документа или раздела. |
| [EndnotePosition](../com.aspose.words/endnoteposition) | Определяет положение концевой сноски. |
| [ExportFontFormat](../com.aspose.words/exportfontformat) | Указывает формат, который используется для экспорта шрифтов при отображении в фиксированный формат HTML. |
| [ExportHeadersFootersMode](../com.aspose.words/exportheadersfootersmode) | Указывает, как верхние и нижние колонтитулы экспортируются в HTML, MHTML или EPUB. |
| [ExportListLabels](../com.aspose.words/exportlistlabels) | Указывает, как метки списков экспортируются в форматы HTML, MHTML и EPUB. |
| [Field](../com.aspose.words/field) | Представляет поле документа Microsoft Word. |
| [FieldAddIn](../com.aspose.words/fieldaddin) | Реализует поле ADDIN. |
| [FieldAddressBlock](../com.aspose.words/fieldaddressblock) | Реализует поле ADDRESSBLOCK. |
| [FieldAdvance](../com.aspose.words/fieldadvance) | Реализует поле ADVANCE. |
| [FieldArgumentBuilder](../com.aspose.words/fieldargumentbuilder) | Создает сложный аргумент поля, состоящий из полей, узлов и простого текста. |
| [FieldAsk](../com.aspose.words/fieldask) | Реализует поле ASK. |
| [FieldAuthor](../com.aspose.words/fieldauthor) | Реализует поле AUTHOR. |
| [FieldAutoNum](../com.aspose.words/fieldautonum) | Реализует поле AUTONUM. |
| [FieldAutoNumLgl](../com.aspose.words/fieldautonumlgl) | Реализует поле AUTONUMLGL. |
| [FieldAutoNumOut](../com.aspose.words/fieldautonumout) | Реализует поле AUTONUMOUT. |
| [FieldAutoText](../com.aspose.words/fieldautotext) | Реализует поле АВТОТЕКСТ. |
| [FieldAutoTextList](../com.aspose.words/fieldautotextlist) | Реализует поле АВТОТЕКСТЛИСТ. |
| [FieldBarcode](../com.aspose.words/fieldbarcode) | Реализует поле ШТРИХ-КОД. |
| [FieldBibliography](../com.aspose.words/fieldbibliography) | Реализует поле БИБЛИОГРАФИЯ. |
| [FieldBidiOutline](../com.aspose.words/fieldbidioutline) | Реализует поле BIDIOUTLINE. |
| [FieldBuilder](../com.aspose.words/fieldbuilder) | Создает поле из токенов кода поля (аргументы и переключатели). |
| [FieldChar](../com.aspose.words/fieldchar) | Базовый класс для узлов, представляющих символы поля в документе. |
| [FieldCitation](../com.aspose.words/fieldcitation) | Реализует поле CITATION. |
| [FieldCollection](../com.aspose.words/fieldcollection) |  Коллекция[Field](../com.aspose.words/field) объекты, представляющие поля в указанном диапазоне. |
| [FieldComments](../com.aspose.words/fieldcomments) | Реализует поле КОММЕНТАРИИ. |
| [FieldCompare](../com.aspose.words/fieldcompare) | Реализует поле СРАВНИТЬ. |
| [FieldCreateDate](../com.aspose.words/fieldcreatedate) | Реализует поле CREATEDATE. |
| [FieldData](../com.aspose.words/fielddata) | Реализует поле DATA. |
| [FieldDatabase](../com.aspose.words/fielddatabase) | Реализует поле DATABASE. |
| [FieldDatabaseDataRow](../com.aspose.words/fielddatabasedatarow) |  Предоставляет данные для[FieldDatabase](../com.aspose.words/fielddatabase) полевой результат. |
| [FieldDatabaseDataTable](../com.aspose.words/fielddatabasedatatable) |  Предоставляет данные для[FieldDatabase](../com.aspose.words/fielddatabase) полевой результат. |
| [FieldDate](../com.aspose.words/fielddate) | Реализует поле DATE. |
| [FieldDde](../com.aspose.words/fielddde) | Реализует поле DDE. |
| [FieldDdeAuto](../com.aspose.words/fieldddeauto) | Реализует поле DDEAUTO. |
| [FieldDisplayBarcode](../com.aspose.words/fielddisplaybarcode) | Реализует поле DISPLAYBARCODE. |
| [FieldDocProperty](../com.aspose.words/fielddocproperty) | Реализует поле DOCPROPERTY. |
| [FieldDocVariable](../com.aspose.words/fielddocvariable) | Реализует поле DOCVARIABLE. |
| [FieldEQ](../com.aspose.words/fieldeq) | Реализует поле эквалайзера. |
| [FieldEditTime](../com.aspose.words/fieldedittime) | Реализует поле EDITTIME. |
| [FieldEmbed](../com.aspose.words/fieldembed) | Реализует поле EMBED. |
| [FieldEnd](../com.aspose.words/fieldend) | Представляет конец поля Word в документе. |
| [FieldFileName](../com.aspose.words/fieldfilename) | Реализует поле FILENAME. |
| [FieldFileSize](../com.aspose.words/fieldfilesize) | Реализует поле FILESIZE. |
| [FieldFillIn](../com.aspose.words/fieldfillin) | Реализует поле FILLIN. |
| [FieldFootnoteRef](../com.aspose.words/fieldfootnoteref) | Реализует поле FOOTNOTEREF. |
| [FieldFormCheckBox](../com.aspose.words/fieldformcheckbox) | Реализует поле FORMCHECKBOX. |
| [FieldFormDropDown](../com.aspose.words/fieldformdropdown) | Реализует поле FORMDROPDOWN. |
| [FieldFormText](../com.aspose.words/fieldformtext) | Реализует поле FORMTEXT. |
| [FieldFormat](../com.aspose.words/fieldformat) | Предоставляет типизированный доступ к числовым значениям поля, дате и времени, а также к общему форматированию. |
| [FieldFormula](../com.aspose.words/fieldformula) | Реализует поле = (формула). |
| [FieldGlossary](../com.aspose.words/fieldglossary) | Реализует поле ГЛОССАРИЙ. |
| [FieldGoToButton](../com.aspose.words/fieldgotobutton) | Реализует поле GOTOBUTTON. |
| [FieldGreetingLine](../com.aspose.words/fieldgreetingline) | Реализует поле GREETINGLINE. |
| [FieldHyperlink](../com.aspose.words/fieldhyperlink) | Реализует поле HYPERLINK |
| [FieldIf](../com.aspose.words/fieldif) | Реализует поле ЕСЛИ. |
| [FieldIfComparisonResult](../com.aspose.words/fieldifcomparisonresult) | Указывает результат оценки условия поля IF. |
| [FieldImport](../com.aspose.words/fieldimport) | Реализует поле ИМПОРТ. |
| [FieldInclude](../com.aspose.words/fieldinclude) | Реализует поле INCLUDE. |
| [FieldIncludePicture](../com.aspose.words/fieldincludepicture) | Реализует поле INCLUDEPICTURE. |
| [FieldIncludeText](../com.aspose.words/fieldincludetext) | Реализует поле INCLUDETEXT. |
| [FieldIndex](../com.aspose.words/fieldindex) | Реализует поле ИНДЕКС. |
| [FieldIndexFormat](../com.aspose.words/fieldindexformat) |  Задает форматирование для[FieldIndex](../com.aspose.words/fieldindex) поля в документе. |
| [FieldInfo](../com.aspose.words/fieldinfo) | Реализует поле INFO. |
| [FieldKeywords](../com.aspose.words/fieldkeywords) | Реализует поле KEYWORDS. |
| [FieldLastSavedBy](../com.aspose.words/fieldlastsavedby) | Реализует поле LASTSAVEDBY. |
| [FieldLink](../com.aspose.words/fieldlink) | Реализует поле ССЫЛКА. |
| [FieldListNum](../com.aspose.words/fieldlistnum) | Реализует поле LISTNUM. |
| [FieldMacroButton](../com.aspose.words/fieldmacrobutton) | Реализует поле MACROBUTTON. |
| [FieldMergeBarcode](../com.aspose.words/fieldmergebarcode) | Реализует поле MERGEBARCODE. |
| [FieldMergeField](../com.aspose.words/fieldmergefield) | Реализует поле MERGEFIELD. |
| [FieldMergeRec](../com.aspose.words/fieldmergerec) | Реализует поле MERGEREC. |
| [FieldMergeSeq](../com.aspose.words/fieldmergeseq) | Реализует поле MERGESEQ. |
| [FieldMergingArgs](../com.aspose.words/fieldmergingargs) |  Предоставляет данные для**MergeField** мероприятие. |
| [FieldMergingArgsBase](../com.aspose.words/fieldmergingargsbase) |  Базовый класс для[FieldMergingArgs](../com.aspose.words/fieldmergingargs) а также[ImageFieldMergingArgs](../com.aspose.words/imagefieldmergingargs). |
| [FieldNext](../com.aspose.words/fieldnext) | Реализует поле NEXT. |
| [FieldNextIf](../com.aspose.words/fieldnextif) | Реализует поле NEXTIF. |
| [FieldNoteRef](../com.aspose.words/fieldnoteref) | Реализует поле NOTEREF. |
| [FieldNumChars](../com.aspose.words/fieldnumchars) | Реализует поле NUMCHARS. |
| [FieldNumPages](../com.aspose.words/fieldnumpages) | Реализует поле NUMPAGES. |
| [FieldNumWords](../com.aspose.words/fieldnumwords) | Реализует поле NUMWORDS. |
| [FieldOcx](../com.aspose.words/fieldocx) | Реализует поле OCX. |
| [FieldOptions](../com.aspose.words/fieldoptions) | Представляет параметры для управления обработкой полей в документе. |
| [FieldPage](../com.aspose.words/fieldpage) | Реализует поле PAGE. |
| [FieldPageRef](../com.aspose.words/fieldpageref) | Реализует поле PAGEREF. |
| [FieldPrint](../com.aspose.words/fieldprint) | Реализует поле PRINT. |
| [FieldPrintDate](../com.aspose.words/fieldprintdate) | Реализует поле PRINTDATE. |
| [FieldPrivate](../com.aspose.words/fieldprivate) | Реализует поле PRIVATE. |
| [FieldQuote](../com.aspose.words/fieldquote) | Реализует поле ЦИТАТА. |
| [FieldRD](../com.aspose.words/fieldrd) | Реализует поле RD. |
| [FieldRef](../com.aspose.words/fieldref) | Реализует поле REF. |
| [FieldRevNum](../com.aspose.words/fieldrevnum) | Реализует поле REVNUM. |
| [FieldSaveDate](../com.aspose.words/fieldsavedate) | Реализует поле SAVEDATE. |
| [FieldSection](../com.aspose.words/fieldsection) | Реализует поле SECTION. |
| [FieldSectionPages](../com.aspose.words/fieldsectionpages) | Реализует поле SECTIONPAGES. |
| [FieldSeparator](../com.aspose.words/fieldseparator) | Представляет разделитель полей Word, который отделяет код поля от результата поля. |
| [FieldSeq](../com.aspose.words/fieldseq) | Реализует поле SEQ. |
| [FieldSet](../com.aspose.words/fieldset) | Реализует поле SET. |
| [FieldShape](../com.aspose.words/fieldshape) | Реализует поле SHAPE. |
| [FieldSkipIf](../com.aspose.words/fieldskipif) | Реализует поле SKIPIF. |
| [FieldStart](../com.aspose.words/fieldstart) | Представляет начало поля Word в документе. |
| [FieldStyleRef](../com.aspose.words/fieldstyleref) | Реализует поле STYLEREF. |
| [FieldSubject](../com.aspose.words/fieldsubject) | Реализует поле SUBJECT. |
| [FieldSymbol](../com.aspose.words/fieldsymbol) | Реализует поле SYMBOL. |
| [FieldTA](../com.aspose.words/fieldta) | Реализует поле ТА. |
| [FieldTC](../com.aspose.words/fieldtc) | Реализует поле TC. |
| [FieldTemplate](../com.aspose.words/fieldtemplate) | Реализует поле ШАБЛОН. |
| [FieldTime](../com.aspose.words/fieldtime) | Реализует поле ВРЕМЯ. |
| [FieldTitle](../com.aspose.words/fieldtitle) | Реализует поле TITLE. |
| [FieldToa](../com.aspose.words/fieldtoa) | Реализует поле TOA. |
| [FieldToc](../com.aspose.words/fieldtoc) | Реализует поле TOC. |
| [FieldType](../com.aspose.words/fieldtype) | Указывает типы полей Microsoft Word. |
| [FieldUnknown](../com.aspose.words/fieldunknown) | Реализует неизвестное или нераспознанное поле. |
| [FieldUpdateCultureSource](../com.aspose.words/fieldupdateculturesource) | Указывает, какую культуру использовать при обновлении поля. |
| [FieldUserAddress](../com.aspose.words/fielduseraddress) | Реализует поле USERADDRESS. |
| [FieldUserInitials](../com.aspose.words/fielduserinitials) | Реализует поле USERINITIALS. |
| [FieldUserName](../com.aspose.words/fieldusername) | Реализует поле USERNAME. |
| [FieldXE](../com.aspose.words/fieldxe) | Реализует поле XE. |
| [FileCorruptedException](../com.aspose.words/filecorruptedexception) | Возникает во время загрузки документа, когда документ кажется поврежденным и его невозможно загрузить. |
| [FileFontSource](../com.aspose.words/filefontsource) | Представляет один файл шрифта TrueType, хранящийся в файловой системе. |
| [FileFormatInfo](../com.aspose.words/fileformatinfo) | Содержит данные, возвращаемые[FileFormatUtil](../com.aspose.words/fileformatutil) методы определения формата документа. |
| [FileFormatUtil](../com.aspose.words/fileformatutil) | Предоставляет служебные методы для работы с форматами файлов, такие как определение формата файла или преобразование расширений файлов в перечисления форматов файлов и из них. |
| [Fill](../com.aspose.words/fill) | Представляет форматирование заливки для объекта. |
| [FillType](../com.aspose.words/filltype) | Указывает тип заполнения для заполняемого объекта. |
| [FindReplaceDirection](../com.aspose.words/findreplacedirection) | Задает направление для операций замены. |
| [FindReplaceOptions](../com.aspose.words/findreplaceoptions) | Задает параметры операций поиска/замены. |
| [FipsUnapprovedOperationException](../com.aspose.words/fipsunapprovedoperationexception) |  |
| [FixedPageSaveOptions](../com.aspose.words/fixedpagesaveoptions) | Содержит общие параметры, которые можно указать при сохранении документа в фиксированных форматах страниц (PDF, XPS, изображения и т. д.). |
| [FlipOrientation](../com.aspose.words/fliporientation) | Возможные значения для ориентации фигуры. |
| [FolderFontSource](../com.aspose.words/folderfontsource) | Представляет папку, содержащую файлы шрифтов TrueType. |
| [Font](../com.aspose.words/font) | Содержит атрибуты шрифта (имя шрифта, размер шрифта, цвет и т. д.) для объекта. |
| [FontConfigSubstitutionRule](../com.aspose.words/fontconfigsubstitutionrule) | Правило подстановки конфигурации шрифта. |
| [FontFallbackSettings](../com.aspose.words/fontfallbacksettings) | Задает настройки резервного механизма шрифта. |
| [FontFamily](../com.aspose.words/fontfamily) | Представляет семейство шрифтов. |
| [FontFeature](../com.aspose.words/fontfeature) |  |
| [FontInfo](../com.aspose.words/fontinfo) | Задает информацию о шрифте, используемом в документе. |
| [FontInfoCollection](../com.aspose.words/fontinfocollection) | Представляет набор шрифтов, используемых в документе. |
| [FontInfoSubstitutionRule](../com.aspose.words/fontinfosubstitutionrule) | Правило подстановки информации о шрифте. |
| [FontNameSubstitutionRule](../com.aspose.words/fontnamesubstitutionrule) | Правило подстановки шрифта для обработки имени шрифта. |
| [FontPitch](../com.aspose.words/fontpitch) | Представляет шаг шрифта. |
| [FontSavingArgs](../com.aspose.words/fontsavingargs) |  Предоставляет данные для[IFontSavingCallback.\#fontSaving(com.aspose.words.FontSavingArgs)](../com.aspose.words/ifontsavingcallback\#fontSaving-com.aspose.words.FontSavingArgs-) мероприятие. |
| [FontSettings](../com.aspose.words/fontsettings) | Задает настройки шрифта для документа. |
| [FontSourceBase](../com.aspose.words/fontsourcebase) | Это абстрактный базовый класс для классов, которые позволяют пользователю указывать различные источники шрифтов. |
| [FontSourceType](../com.aspose.words/fontsourcetype) | Указывает тип источника шрифта. |
| [FontSubstitutionRule](../com.aspose.words/fontsubstitutionrule) | Это абстрактный базовый класс для правила подстановки шрифта. |
| [FontSubstitutionSettings](../com.aspose.words/fontsubstitutionsettings) | Задает настройки механизма подстановки шрифтов. |
| [Footnote](../com.aspose.words/footnote) | Представляет контейнер для текста сноски или концевой сноски. |
| [FootnoteNumberingRule](../com.aspose.words/footnotenumberingrule) | Определяет, когда автоматически возобновляется нумерация сносок или концевых сносок. |
| [FootnoteOptions](../com.aspose.words/footnoteoptions) | Представляет параметры нумерации сносок для документа или раздела. |
| [FootnotePosition](../com.aspose.words/footnoteposition) | Определяет положение сноски. |
| [FootnoteType](../com.aspose.words/footnotetype) | Указывает, является ли это сноской или концевой сноской. |
| [FormField](../com.aspose.words/formfield) | Представляет одно поле формы. |
| [FormFieldCollection](../com.aspose.words/formfieldcollection) |  Коллекция**FormField** объекты, которые представляют все поля формы в диапазоне. |
| [Forms2OleControl](../com.aspose.words/forms2olecontrol) | Представляет элемент управления OLE Microsoft Forms 2.0. |
| [Forms2OleControlCollection](../com.aspose.words/forms2olecontrolcollection) |  Представляет собой коллекцию[Forms2OleControl](../com.aspose.words/forms2olecontrol) объекты. |
| [Forms2OleControlType](../com.aspose.words/forms2olecontroltype) |  |
| [FrameFormat](../com.aspose.words/frameformat) | Представляет форматирование абзаца, связанное с фреймом. |
| [Frameset](../com.aspose.words/frameset) |  |
| [FramesetCollection](../com.aspose.words/framesetcollection) |  |
| [GeneralFormat](../com.aspose.words/generalformat) | Задает общий формат, который применяется к числовому, текстовому или любому результату поля. |
| [GeneralFormatCollection](../com.aspose.words/generalformatcollection) | Представляет типизированную коллекцию общих форматов. |
| [GlossaryDocument](../com.aspose.words/glossarydocument) | Представляет корневой элемент документа глоссария в документе Word. |
| [Glyph](../com.aspose.words/glyph) |  |
| [GradientStop](../com.aspose.words/gradientstop) | Представляет одну остановку градиента. |
| [GradientStopCollection](../com.aspose.words/gradientstopcollection) |  Содержит коллекцию[GradientStop](../com.aspose.words/gradientstop) объекты. |
| [GradientStyle](../com.aspose.words/gradientstyle) | Задает стиль градиентной заливки. |
| [GradientVariant](../com.aspose.words/gradientvariant) | Указывает вариант градиентной заливки. |
| [Granularity](../com.aspose.words/granularity) | Задает степень детализации изменений для отслеживания при сравнении двух документов. |
| [GraphicsQualityOptions](../com.aspose.words/graphicsqualityoptions) | Позволяет указать доп. |
| [GroupShape](../com.aspose.words/groupshape) | Представляет группу фигур в документе. |
| [HeaderFooter](../com.aspose.words/headerfooter) | Представляет контейнер для текста верхнего или нижнего колонтитула раздела. |
| [HeaderFooterBookmarksExportMode](../com.aspose.words/headerfooterbookmarksexportmode) | Указывает, как экспортируются закладки в верхних/нижних колонтитулах. |
| [HeaderFooterCollection](../com.aspose.words/headerfootercollection) |  Предоставляет типизированный доступ к[HeaderFooter](../com.aspose.words/headerfooter) узлы**Section**. |
| [HeaderFooterType](../com.aspose.words/headerfootertype) | Определяет тип верхнего или нижнего колонтитула в файле Word. |
| [HeightRule](../com.aspose.words/heightrule) | Задает правило определения высоты объекта. |
| [HorizontalAlignment](../com.aspose.words/horizontalalignment) | Задает горизонтальное выравнивание плавающей фигуры, текстового фрейма или плавающей таблицы. |
| [HorizontalRuleAlignment](../com.aspose.words/horizontalrulealignment) | Представляет выравнивание для указанной горизонтальной линейки. |
| [HorizontalRuleFormat](../com.aspose.words/horizontalruleformat) | Представляет форматирование горизонтальной линейки. |
| [HtmlControlType](../com.aspose.words/htmlcontroltype) | Тип узлов документа, представляющих и элементы, импортированные из HTML. |
| [HtmlElementSizeOutputMode](../com.aspose.words/htmlelementsizeoutputmode) | Указывает, как Aspose.Words экспортирует ширину и высоту элементов в HTML, MHTML и EPUB. |
| [HtmlFixedPageHorizontalAlignment](../com.aspose.words/htmlfixedpagehorizontalalignment) | Задает горизонтальное выравнивание страниц в выходном HTML-документе. |
| [HtmlFixedSaveOptions](../com.aspose.words/htmlfixedsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#HTML\_FIXED](../com.aspose.words/saveformat\#HTML-FIXED) формат. |
| [HtmlInsertOptions](../com.aspose.words/htmlinsertoptions) |  Задает параметры для**M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)** метод. |
| [HtmlLoadOptions](../com.aspose.words/htmlloadoptions) |  Позволяет указать дополнительные параметры при загрузке HTML-документа в[Document](../com.aspose.words/document) объект. |
| [HtmlMetafileFormat](../com.aspose.words/htmlmetafileformat) | Указывает формат, в котором метафайлы сохраняются в документах HTML. |
| [HtmlOfficeMathOutputMode](../com.aspose.words/htmlofficemathoutputmode) | Указывает, как Aspose.Words экспортирует OfficeMath в HTML, MHTML и EPUB. |
| [HtmlSaveOptions](../com.aspose.words/htmlsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#HTML](../com.aspose.words/saveformat\#HTML), [SaveFormat.\#MHTML](../com.aspose.words/saveformat\#MHTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat\#EPUB) или же[SaveFormat.\#AZW\_3](../com.aspose.words/saveformat\#AZW-3) формат. |
| [HtmlVersion](../com.aspose.words/htmlversion) |  Указывает версию HTML, используемую при сохранении документа в[SaveFormat.\#HTML](../com.aspose.words/saveformat\#HTML) а также[SaveFormat.\#MHTML](../com.aspose.words/saveformat\#MHTML) форматы. |
| [Hyphenation](../com.aspose.words/hyphenation) | Предоставляет методы для работы со словарями переносов. |
| [HyphenationOptions](../com.aspose.words/hyphenationoptions) | Позволяет настроить параметры переноса документа. |
| [ImageBinarizationMethod](../com.aspose.words/imagebinarizationmethod) | Указывает метод, используемый для бинаризации изображения. |
| [ImageColorMode](../com.aspose.words/imagecolormode) | Указывает цветовой режим для сгенерированных изображений страниц документа. |
| [ImageData](../com.aspose.words/imagedata) | Определяет изображение для фигуры. |
| [ImageFieldMergingArgs](../com.aspose.words/imagefieldmergingargs) |  Предоставляет данные для[IFieldMergingCallback.\#imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../com.aspose.words/ifieldmergingcallback\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs-) мероприятие. |
| [ImagePixelFormat](../com.aspose.words/imagepixelformat) | Указывает формат пикселей для сгенерированных изображений страниц документа. |
| [ImageSaveOptions](../com.aspose.words/imagesaveoptions) | Позволяет указать дополнительные параметры при преобразовании страниц документа или фигур в изображения. |
| [ImageSavingArgs](../com.aspose.words/imagesavingargs) |  Предоставляет данные для[IImageSavingCallback.\#imageSaving(com.aspose.words.ImageSavingArgs)](../com.aspose.words/iimagesavingcallback\#imageSaving-com.aspose.words.ImageSavingArgs-) мероприятие. |
| [ImageSize](../com.aspose.words/imagesize) | Содержит информацию о размере и разрешении изображения. |
| [ImageType](../com.aspose.words/imagetype) | Указывает тип (формат) изображения в документе Microsoft Word. |
| [ImageWatermarkOptions](../com.aspose.words/imagewatermarkoptions) | Содержит параметры, которые можно указать при добавлении водяного знака с изображением. |
| [ImlRenderingMode](../com.aspose.words/imlrenderingmode) | Указывает, как объекты рукописного ввода (InkML) отображаются в фиксированных форматах страниц. |
| [ImportFormatMode](../com.aspose.words/importformatmode) | Указывает, как форматирование объединяется при импорте содержимого из другого документа. |
| [ImportFormatOptions](../com.aspose.words/importformatoptions) | Позволяет указать различные параметры импорта для форматирования вывода. |
| [IncorrectPasswordException](../com.aspose.words/incorrectpasswordexception) | Возникает, если документ зашифрован паролем, а пароль, указанный при открытии документа, неверный или отсутствует. |
| [Inline](../com.aspose.words/inline) | Базовый класс для узлов встроенного уровня, которые могут иметь связанное с ними форматирование символов, но не могут иметь собственных дочерних узлов. |
| [InlineStory](../com.aspose.words/inlinestory) | Базовый класс для узлов встроенного уровня, которые могут содержать абзацы и таблицы. |
| [InternableComplexAttr](../com.aspose.words/internablecomplexattr) | Базовый класс для внутреннего сложного атрибута. |
| [JoinStyle](../com.aspose.words/joinstyle) | Стиль соединения линий. |
| [JsonDataLoadOptions](../com.aspose.words/jsondataloadoptions) | Представляет параметры анализа данных JSON. |
| [JsonDataSource](../com.aspose.words/jsondatasource) | Предоставляет доступ к данным файла или потока JSON для использования в отчете. |
| [JsonSimpleValueParseMode](../com.aspose.words/jsonsimplevalueparsemode) | Указывает режим анализа простых значений JSON (пустых, логических, числовых, целых и строковых) при загрузке JSON. |
| [KnownTypeSet](../com.aspose.words/knowntypeset) | Представляет неупорядоченный набор (т.е. |
| [LanguagePreferences](../com.aspose.words/languagepreferences) | Позволяет настроить языковые настройки. |
| [LayoutCollector](../com.aspose.words/layoutcollector) | Этот класс позволяет вычислять номера страниц узлов документа. |
| [LayoutEntityType](../com.aspose.words/layoutentitytype) | Типы объектов макета. |
| [LayoutEnumerator](../com.aspose.words/layoutenumerator) | Перечисляет объекты макета страницы документа. |
| [LayoutFlow](../com.aspose.words/layoutflow) | Определяет поток макета текста в текстовом поле. |
| [LayoutOptions](../com.aspose.words/layoutoptions) | Содержит параметры, позволяющие управлять процессом верстки документа. |
| [LegendPosition](../com.aspose.words/legendposition) | Определяет возможные позиции легенды диаграммы. |
| [License](../com.aspose.words/license) | Предоставляет методы для лицензирования компонента. |
| [LineNumberRestartMode](../com.aspose.words/linenumberrestartmode) | Определяет, когда перезапускается автоматическая нумерация строк. |
| [LineSpacingRule](../com.aspose.words/linespacingrule) | Указывает значения межстрочного интервала для абзаца. |
| [LineStyle](../com.aspose.words/linestyle) |  Определяет стиль линии[Border](../com.aspose.words/border). |
| [List](../com.aspose.words/list) | Представляет форматирование списка. |
| [ListCollection](../com.aspose.words/listcollection) | Хранит и управляет форматированием маркированных и нумерованных списков, используемых в документе. |
| [ListFormat](../com.aspose.words/listformat) | Позволяет контролировать, какое форматирование списка применяется к абзацу. |
| [ListLabel](../com.aspose.words/listlabel) | Определяет свойства, специфичные для метки списка. |
| [ListLevel](../com.aspose.words/listlevel) | Определяет форматирование для уровня списка. |
| [ListLevelAlignment](../com.aspose.words/listlevelalignment) | Указывает выравнивание для номера списка или маркера. |
| [ListLevelCollection](../com.aspose.words/listlevelcollection) | Коллекция форматирования списка для каждого уровня в списке. |
| [ListTemplate](../com.aspose.words/listtemplate) | Указывает один из предопределенных форматов списка, доступных в Microsoft Word. |
| [ListTrailingCharacter](../com.aspose.words/listtrailingcharacter) | Задает символ, отделяющий метку списка от текста абзаца. |
| [LoadFormat](../com.aspose.words/loadformat) | Указывает формат загружаемого документа. |
| [LoadOptions](../com.aspose.words/loadoptions) |  Позволяет указать дополнительные параметры (например, пароль или базовый URI) при загрузке документа в[Document](../com.aspose.words/document) объект. |
| [MailMerge](../com.aspose.words/mailmerge) | Представляет функцию слияния почты. |
| [MailMergeCheckErrors](../com.aspose.words/mailmergecheckerrors) | Указывает, как Microsoft Word будет сообщать об ошибках, обнаруженных во время слияния. |
| [MailMergeCleanupOptions](../com.aspose.words/mailmergecleanupoptions) | Задает параметры, определяющие, какие элементы удаляются при слиянии почты. |
| [MailMergeDataType](../com.aspose.words/mailmergedatatype) | Указывает тип внешнего источника данных слияния почты. |
| [MailMergeDestination](../com.aspose.words/mailmergedestination) | Определяет возможные результаты, которые могут быть получены при выполнении слияния для документа. |
| [MailMergeMainDocumentType](../com.aspose.words/mailmergemaindocumenttype) | Указывает возможные типы исходного документа слияния. |
| [MailMergeRegionInfo](../com.aspose.words/mailmergeregioninfo) | Содержит информацию о регионе слияния. |
| [MailMergeSettings](../com.aspose.words/mailmergesettings) | Указывает всю информацию о слиянии для документа. |
| [MappedDataFieldCollection](../com.aspose.words/mappeddatafieldcollection) | Позволяет автоматически сопоставлять имена полей в вашем источнике данных и имена полей слияния в документе. |
| [MarkdownSaveOptions](../com.aspose.words/markdownsaveoptions) |  Класс для указания дополнительных параметров при сохранении документа в[SaveFormat.\#MARKDOWN](../com.aspose.words/saveformat\#MARKDOWN) формат. |
| [MarkerSymbol](../com.aspose.words/markersymbol) | Задает стиль символа маркера. |
| [MarkupLevel](../com.aspose.words/markuplevel) |  Определяет уровень в дереве документа, на котором[StructuredDocumentTag](../com.aspose.words/structureddocumenttag) может возникнуть. |
| [MathObjectType](../com.aspose.words/mathobjecttype) | Указывает тип объекта Office Math. |
| [MeasurementUnits](../com.aspose.words/measurementunits) | Задает единицу измерения. |
| [MemoryFontSource](../com.aspose.words/memoryfontsource) | Представляет один файл шрифта TrueType, хранящийся в памяти. |
| [MergeFieldImageDimension](../com.aspose.words/mergefieldimagedimension) | Представляет размер изображения (т.е. |
| [MergeFieldImageDimensionUnit](../com.aspose.words/mergefieldimagedimensionunit) | Определяет единицу измерения изображения (т.е. |
| [MetafileRenderingMode](../com.aspose.words/metafilerenderingmode) | Указывает, как Aspose.Words должен отображать метафайлы WMF и EMF. |
| [MetafileRenderingOptions](../com.aspose.words/metafilerenderingoptions) | Позволяет указать дополнительные параметры рендеринга метафайла. |
| [Metered](../com.aspose.words/metered) | Предоставляет методы для установки измеренного ключа. |
| [MsWordVersion](../com.aspose.words/mswordversion) | Позволяет Aspose.Wods имитировать поведение приложения в зависимости от версии MS Word. |
| [MultiplePagesType](../com.aspose.words/multiplepagestype) | Указывает, как распечатывается документ. |
| [Node](../com.aspose.words/node) | Базовый класс для всех узлов документа Word. |
| [NodeChangingAction](../com.aspose.words/nodechangingaction) | Указывает тип изменения узла. |
| [NodeChangingArgs](../com.aspose.words/nodechangingargs) |  Предоставляет данные для методов[INodeChangingCallback](../com.aspose.words/inodechangingcallback) интерфейс. |
| [NodeCollection](../com.aspose.words/nodecollection) | Представляет набор узлов определенного типа. |
| [NodeImporter](../com.aspose.words/nodeimporter) | Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой. |
| [NodeList](../com.aspose.words/nodelist) |  Представляет набор узлов, соответствующих запросу XPath, выполненному с использованием[CompositeNode.\#selectNodes(java.lang.String)](../com.aspose.words/compositenode\#selectNodes-java.lang.String-) метод. |
| [NodeRendererBase](../com.aspose.words/noderendererbase) |  Базовый класс для[ShapeRenderer](../com.aspose.words/shaperenderer) а также[OfficeMathRenderer](../com.aspose.words/officemathrenderer). |
| [NodeType](../com.aspose.words/nodetype) | Указывает тип узла документа Word. |
| [NumberStyle](../com.aspose.words/numberstyle) | Определяет стиль номеров для списка, сносок и концевых сносок, номеров страниц. |
| [NumeralFormat](../com.aspose.words/numeralformat) | Указывает набор символов, который используется для представления чисел при отображении в фиксированных форматах страниц. |
| [Odso](../com.aspose.words/odso) | Указывает параметры объекта источника данных Office (ODSO) для источника данных слияния. |
| [OdsoDataSourceType](../com.aspose.words/odsodatasourcetype) | Указывает тип внешнего источника данных, к которому необходимо подключиться, как часть информации о соединении ODSO. |
| [OdsoFieldMapData](../com.aspose.words/odsofieldmapdata) | Указывает, как столбец во внешнем источнике данных должен быть сопоставлен с предопределенными полями слияния в документе. |
| [OdsoFieldMapDataCollection](../com.aspose.words/odsofieldmapdatacollection) | Типизированная коллекция[OdsoFieldMapData](../com.aspose.words/odsofieldmapdata) объекты. |
| [OdsoFieldMappingType](../com.aspose.words/odsofieldmappingtype) | Указывает возможные типы, используемые для указания, сопоставлено ли данное поле слияния со столбцом в данном внешнем источнике данных. |
| [OdsoRecipientData](../com.aspose.words/odsorecipientdata) | Представляет информацию об одной записи во внешнем источнике данных, которая должна быть исключена из слияния. |
| [OdsoRecipientDataCollection](../com.aspose.words/odsorecipientdatacollection) |  Типизированная коллекция[OdsoRecipientData](../com.aspose.words/odsorecipientdata) |
| [OdtSaveMeasureUnit](../com.aspose.words/odtsavemeasureunit) | Заданные единицы измерения для применения к измеримому содержимому документа, такому как форма, ширина и т. д., во время сохранения. |
| [OdtSaveOptions](../com.aspose.words/odtsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#ODT](../com.aspose.words/saveformat\#ODT) или же[SaveFormat.\#OTT](../com.aspose.words/saveformat\#OTT) формат. |
| [OfficeMath](../com.aspose.words/officemath) | Представляет объект Office Math, такой как функция, уравнение, матрица и т.п. |
| [OfficeMathDisplayType](../com.aspose.words/officemathdisplaytype) | Указывает тип формата отображения уравнения. |
| [OfficeMathJustification](../com.aspose.words/officemathjustification) | Задает обоснование уравнения. |
| [OfficeMathRenderer](../com.aspose.words/officemathrenderer) |  Предоставляет методы для отображения отдельных[OfficeMath](../com.aspose.words/officemath) в растровое или векторное изображение или в объект Graphics. |
| [OleControl](../com.aspose.words/olecontrol) | Представляет элемент управления OLE ActiveX. |
| [OleFormat](../com.aspose.words/oleformat) | Предоставляет доступ к данным объекта OLE или элемента управления ActiveX. |
| [OlePackage](../com.aspose.words/olepackage) | Позволяет получить доступ к свойствам пакета OLE. |
| [OoxmlCompliance](../com.aspose.words/ooxmlcompliance) | Позволяет указать, какая спецификация OOXML будет использоваться при сохранении в формате DOCX. |
| [OoxmlSaveOptions](../com.aspose.words/ooxmlsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#DOCX](../com.aspose.words/saveformat\#DOCX), [SaveFormat.\#DOCM](../com.aspose.words/saveformat\#DOCM), [SaveFormat.\#DOTX](../com.aspose.words/saveformat\#DOTX), [SaveFormat.\#DOTM](../com.aspose.words/saveformat\#DOTM) или же[SaveFormat.\#FLAT\_OPC](../com.aspose.words/saveformat\#FLAT-OPC) формат. |
| [Orientation](../com.aspose.words/orientation) | Задает ориентацию страницы. |
| [OutlineLevel](../com.aspose.words/outlinelevel) | Задает уровень структуры абзаца в документе. |
| [OutlineOptions](../com.aspose.words/outlineoptions) | Позволяет указать параметры контура. |
| [PageBorderAppliesTo](../com.aspose.words/pageborderappliesto) | Указывает, на каких страницах печатается граница страницы. |
| [PageBorderDistanceFrom](../com.aspose.words/pageborderdistancefrom) | Задает положение границы страницы относительно поля страницы. |
| [PageInfo](../com.aspose.words/pageinfo) | Представляет информацию о конкретной странице документа. |
| [PageLayoutCallbackArgs](../com.aspose.words/pagelayoutcallbackargs) |  Аргумент, переданный в[IPageLayoutCallback.\#notify(com.aspose.words.PageLayoutCallbackArgs)](../com.aspose.words/ipagelayoutcallback\#notify-com.aspose.words.PageLayoutCallbackArgs-) |
| [PageLayoutEvent](../com.aspose.words/pagelayoutevent) | Код события, возникающего во время построения и рендеринга модели макета страницы. |
| [PageRange](../com.aspose.words/pagerange) | Представляет непрерывный диапазон страниц. |
| [PageSavingArgs](../com.aspose.words/pagesavingargs) |  Предоставляет данные для[IPageSavingCallback.\#pageSaving(com.aspose.words.PageSavingArgs)](../com.aspose.words/ipagesavingcallback\#pageSaving-com.aspose.words.PageSavingArgs-) мероприятие. |
| [PageSet](../com.aspose.words/pageset) | Описывает случайный набор страниц. |
| [PageSetup](../com.aspose.words/pagesetup) | Представляет свойства настройки страницы раздела. |
| [PageVerticalAlignment](../com.aspose.words/pageverticalalignment) | Задает вертикальное выравнивание текста на каждой странице. |
| [PaperSize](../com.aspose.words/papersize) | Задает размер бумаги. |
| [Paragraph](../com.aspose.words/paragraph) | Представляет абзац текста. |
| [ParagraphAlignment](../com.aspose.words/paragraphalignment) | Задает выравнивание текста в абзаце. |
| [ParagraphCollection](../com.aspose.words/paragraphcollection) |  Предоставляет типизированный доступ к коллекции[Paragraph](../com.aspose.words/paragraph) узлы. |
| [ParagraphFormat](../com.aspose.words/paragraphformat) | Представляет все форматирование абзаца. |
| [PatternType](../com.aspose.words/patterntype) | Задает образец заливки, который будет использоваться для заливки фигуры. |
| [PclSaveOptions](../com.aspose.words/pclsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#PCL](../com.aspose.words/saveformat\#PCL) формат. |
| [PdfCompliance](../com.aspose.words/pdfcompliance) | Указывает уровень соответствия стандартам PDF. |
| [PdfCustomPropertiesExport](../com.aspose.words/pdfcustompropertiesexport) |  Указывает способ[Document.\#getCustomDocumentProperties()](../com.aspose.words/document\#getCustomDocumentProperties--) экспортируются в файл PDF. |
| [PdfDigitalSignatureDetails](../com.aspose.words/pdfdigitalsignaturedetails) | Содержит сведения о подписании документа PDF цифровой подписью. |
| [PdfDigitalSignatureHashAlgorithm](../com.aspose.words/pdfdigitalsignaturehashalgorithm) | Задает алгоритм цифрового хеширования, используемый цифровой подписью. |
| [PdfDigitalSignatureTimestampSettings](../com.aspose.words/pdfdigitalsignaturetimestampsettings) | Содержит настройки временной метки цифровой подписи. |
| [PdfEncryptionDetails](../com.aspose.words/pdfencryptiondetails) | Содержит сведения о шифровании и разрешениях на доступ к PDF-документу. |
| [PdfFontEmbeddingMode](../com.aspose.words/pdffontembeddingmode) | Указывает, как Aspose.Words должен встраивать шрифты. |
| [PdfImageColorSpaceExportMode](../com.aspose.words/pdfimagecolorspaceexportmode) | Указывает, как цветовое пространство будет выбрано для изображений в документе PDF. |
| [PdfImageCompression](../com.aspose.words/pdfimagecompression) | Указывает тип сжатия, применяемый к изображениям в файле PDF. |
| [PdfLoadOptions](../com.aspose.words/pdfloadoptions) |  Позволяет указать дополнительные параметры при загрузке документа Pdf в[Document](../com.aspose.words/document) объект. |
| [PdfPageMode](../com.aspose.words/pdfpagemode) | Указывает, как документ PDF должен отображаться при открытии в программе чтения PDF. |
| [PdfPermissions](../com.aspose.words/pdfpermissions) | Определяет операции, разрешенные пользователю для зашифрованного PDF-документа. |
| [PdfSaveOptions](../com.aspose.words/pdfsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#PDF](../com.aspose.words/saveformat\#PDF) формат. |
| [PdfTextCompression](../com.aspose.words/pdftextcompression) | Указывает тип сжатия, применяемый ко всему содержимому файла PDF, кроме изображений. |
| [PdfZoomBehavior](../com.aspose.words/pdfzoombehavior) | Указывает тип масштабирования, применяемый к документу PDF при его открытии в средстве просмотра PDF. |
| [PhysicalFontInfo](../com.aspose.words/physicalfontinfo) | Указывает информацию о физическом шрифте, доступном для шрифтового движка Aspose.Words. |
| [PlainTextDocument](../com.aspose.words/plaintextdocument) | Позволяет извлекать текстовое представление содержимого документа. |
| [PreferredWidth](../com.aspose.words/preferredwidth) | Представляет значение и его единицу измерения, которые используются для указания предпочтительной ширины таблицы или ячейки. |
| [PreferredWidthType](../com.aspose.words/preferredwidthtype) | Задает единицу измерения предпочтительной ширины таблицы или ячейки. |
| [PresetTexture](../com.aspose.words/presettexture) | Указывает текстуру, которая будет использоваться для заполнения формы. |
| [PropertyType](../com.aspose.words/propertytype) | Указывает тип данных свойства документа. |
| [ProtectionType](../com.aspose.words/protectiontype) | Тип защиты документа. |
| [PsSaveOptions](../com.aspose.words/pssaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#PS](../com.aspose.words/saveformat\#PS) формат. |
| [Range](../com.aspose.words/range) | Представляет непрерывную область в документе. |
| [RelativeHorizontalPosition](../com.aspose.words/relativehorizontalposition) | Указывает относительное положение фигуры или текстового фрейма по горизонтали. |
| [RelativeVerticalPosition](../com.aspose.words/relativeverticalposition) | Указывает относительное положение фигуры или текстового фрейма по вертикали. |
| [ReplaceAction](../com.aspose.words/replaceaction) | Позволяет пользователю указать, что происходит с текущим совпадением во время операции замены. |
| [ReplacingArgs](../com.aspose.words/replacingargs) | Предоставляет данные для пользовательской операции замены. |
| [ReportBuildOptions](../com.aspose.words/reportbuildoptions) |  Задает параметры, управляющие поведением[ReportingEngine](../com.aspose.words/reportingengine) при построении отчета. |
| [ReportingEngine](../com.aspose.words/reportingengine) | Предоставляет подпрограммы для заполнения документов-шаблонов данными и набор параметров для управления этими подпрограммами. |
| [ResourceLoadingAction](../com.aspose.words/resourceloadingaction) | Задает режим загрузки ресурсов. |
| [ResourceLoadingArgs](../com.aspose.words/resourceloadingargs) |  Предоставляет данные для[IResourceLoadingCallback.\#resourceLoading(com.aspose.words.ResourceLoadingArgs)](../com.aspose.words/iresourceloadingcallback\#resourceLoading-com.aspose.words.ResourceLoadingArgs-) метод. |
| [ResourceSavingArgs](../com.aspose.words/resourcesavingargs) |  Предоставляет данные для[IResourceSavingCallback.\#resourceSaving(com.aspose.words.ResourceSavingArgs)](../com.aspose.words/iresourcesavingcallback\#resourceSaving-com.aspose.words.ResourceSavingArgs-) мероприятие. |
| [ResourceType](../com.aspose.words/resourcetype) | Тип загружаемого ресурса. |
| [Revision](../com.aspose.words/revision) | Представляет редакцию (отслеживаемое изменение) в узле документа или стиле. |
| [RevisionCollection](../com.aspose.words/revisioncollection) |  Коллекция[Revision](../com.aspose.words/revision) объекты, представляющие исправления в документе. |
| [RevisionColor](../com.aspose.words/revisioncolor) | Позволяет указать цвет ревизий документа. |
| [RevisionGroup](../com.aspose.words/revisiongroup) |  Представляет собой группу последовательных[Revision](../com.aspose.words/revision) объекты. |
| [RevisionGroupCollection](../com.aspose.words/revisiongroupcollection) |  Коллекция[RevisionGroup](../com.aspose.words/revisiongroup) объекты, которые представляют группы ревизий в документе. |
| [RevisionOptions](../com.aspose.words/revisionoptions) | Позволяет контролировать, как обрабатываются версии документа в процессе компоновки. |
| [RevisionTextEffect](../com.aspose.words/revisiontexteffect) | Позволяет указать эффект оформления для редакций текста документа. |
| [RevisionType](../com.aspose.words/revisiontype) |  Указывает тип отслеживаемого изменения[Revision](../com.aspose.words/revision). |
| [RevisionsView](../com.aspose.words/revisionsview) | Позволяет указать, следует ли работать с оригинальной или исправленной версией документа. |
| [Row](../com.aspose.words/row) | Представляет строку таблицы. |
| [RowCollection](../com.aspose.words/rowcollection) |  Предоставляет типизированный доступ к коллекции[Row](../com.aspose.words/row) узлы. |
| [RowFormat](../com.aspose.words/rowformat) | Представляет все форматирование строки таблицы. |
| [RtfLoadOptions](../com.aspose.words/rtfloadoptions) |  Позволяет указать дополнительные параметры при загрузке[LoadFormat.\#RTF](../com.aspose.words/loadformat\#RTF) документ в[Document](../com.aspose.words/document) объект. |
| [RtfSaveOptions](../com.aspose.words/rtfsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#RTF](../com.aspose.words/saveformat\#RTF) формат. |
| [Run](../com.aspose.words/run) | Представляет набор символов с одинаковым форматированием шрифта. |
| [RunCollection](../com.aspose.words/runcollection) |  Предоставляет типизированный доступ к коллекции[Run](../com.aspose.words/run) узлы. |
| [SaveFormat](../com.aspose.words/saveformat) | Указывает формат, в котором сохранен документ. |
| [SaveOptions](../com.aspose.words/saveoptions) | Это абстрактный базовый класс для классов, которые позволяют пользователю указывать дополнительные параметры при сохранении документа в определенном формате. |
| [SaveOutputParameters](../com.aspose.words/saveoutputparameters) | Этот объект возвращается вызывающей стороне после сохранения документа и содержит дополнительную информацию, которая была сгенерирована или рассчитана во время операции сохранения. |
| [ScriptShapingLevel](../com.aspose.words/scriptshapinglevel) |  |
| [SdtAppearance](../com.aspose.words/sdtappearance) | Определяет внешний вид тега структурированного документа. |
| [SdtCalendarType](../com.aspose.words/sdtcalendartype) |  Определяет возможные типы календарей, которые можно использовать для указания[StructuredDocumentTag.\#getCalendarType()](../com.aspose.words/structureddocumenttag\#getCalendarType--) / [StructuredDocumentTag.\#setCalendarType(int)](../com.aspose.words/structureddocumenttag\#setCalendarType-int-) в документе Office Open XML. |
| [SdtDateStorageFormat](../com.aspose.words/sdtdatestorageformat) | Указывает, как дата для SDT даты сохраняется/извлекается, когда SDT привязан к узлу XML в хранилище данных документа. |
| [SdtListItem](../com.aspose.words/sdtlistitem) |  Этот элемент определяет один элемент списка в родительском элементе.[SdtType.\#COMBO\_BOX](../com.aspose.words/sdttype\#COMBO-BOX) или же[SdtType.\#DROP\_DOWN\_LIST](../com.aspose.words/sdttype\#DROP-DOWN-LIST) тег структурированного документа. |
| [SdtListItemCollection](../com.aspose.words/sdtlistitemcollection) |  Обеспечивает доступ к[SdtListItem](../com.aspose.words/sdtlistitem) элементы тега структурированного документа. |
| [SdtType](../com.aspose.words/sdttype) | Задает тип узла тега структурированного документа (SDT). |
| [Section](../com.aspose.words/section) | Представляет один раздел в документе. |
| [SectionCollection](../com.aspose.words/sectioncollection) |  Коллекция**Section** объекты в документе. |
| [SectionLayoutMode](../com.aspose.words/sectionlayoutmode) | Указывает режим макета для раздела, позволяющий определить поведение сетки документа. |
| [SectionStart](../com.aspose.words/sectionstart) | Тип разрыва в начале раздела. |
| [Shading](../com.aspose.words/shading) | Содержит атрибуты затенения для объекта. |
| [ShadowFormat](../com.aspose.words/shadowformat) | Представляет теневое форматирование для объекта. |
| [ShadowType](../com.aspose.words/shadowtype) | Указывает тип тени формы. |
| [Shape](../com.aspose.words/shape) | Представляет объект в слое рисования, например автофигуру, текстовое поле, произвольную форму, объект OLE, элемент управления ActiveX или изображение. |
| [ShapeBase](../com.aspose.words/shapebase) | Базовый класс для объектов на уровне рисования, таких как AutoShape, произвольная форма, объект OLE, элемент управления ActiveX или изображение. |
| [ShapeLineStyle](../com.aspose.words/shapelinestyle) |  Определяет стиль составной линии[Shape](../com.aspose.words/shape). |
| [ShapeMarkupLanguage](../com.aspose.words/shapemarkuplanguage) | Указывает язык разметки, используемый для фигуры. |
| [ShapeRenderer](../com.aspose.words/shaperenderer) |  Предоставляет методы для отображения отдельных[Shape](../com.aspose.words/shape) или же[GroupShape](../com.aspose.words/groupshape) в растровое или векторное изображение или в объект Graphics. |
| [ShapeType](../com.aspose.words/shapetype) | Указывает тип фигуры в документе Microsoft Word. |
| [ShowInBalloons](../com.aspose.words/showinballoons) | Указывает, какие ревизии отображаются во всплывающих подсказках. |
| [SignOptions](../com.aspose.words/signoptions) | Позволяет указать параметры подписания документа. |
| [SignatureLine](../com.aspose.words/signatureline) | Предоставляет доступ к свойствам строки подписи. |
| [SignatureLineOptions](../com.aspose.words/signaturelineoptions) | Позволяет указать параметры для вставляемой строки подписи. |
| [SmartTag](../com.aspose.words/smarttag) | Этот элемент указывает наличие смарт-тега вокруг одной или нескольких встроенных структур (прогонов, изображений, полей и т. д.) внутри абзаца. |
| [SpecialChar](../com.aspose.words/specialchar) | Базовый класс для специальных символов в документе. |
| [Story](../com.aspose.words/story) |  Базовый класс для элементов, содержащих узлы блочного уровня.[Paragraph](../com.aspose.words/paragraph) а также[Table](../com.aspose.words/table). |
| [StoryType](../com.aspose.words/storytype) | Текст документа Word хранится в историях. |
| [StreamFontSource](../com.aspose.words/streamfontsource) | Базовый класс для пользовательского источника потокового шрифта. |
| [Stroke](../com.aspose.words/stroke) | Определяет штрих для фигуры. |
| [StructuredDocumentTag](../com.aspose.words/structureddocumenttag) | Представляет тег структурированного документа (SDT или элемент управления содержимым) в документе. |
| [StructuredDocumentTagCollection](../com.aspose.words/structureddocumenttagcollection) |  Коллекция[IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag) экземпляры, представляющие теги структурированного документа в указанном диапазоне. |
| [StructuredDocumentTagRangeEnd](../com.aspose.words/structureddocumenttagrangeend) |  Представляет собой конец**ranged** тег структурированного документа, который принимает содержимое из нескольких разделов. |
| [StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart) |  Представляет собой начало**ranged** тег структурированного документа, который принимает содержимое из нескольких разделов. |
| [Style](../com.aspose.words/style) | Представляет один встроенный или определяемый пользователем стиль. |
| [StyleCollection](../com.aspose.words/stylecollection) | Коллекция объектов Style, представляющих как встроенные, так и определяемые пользователем стили в документе. |
| [StyleIdentifier](../com.aspose.words/styleidentifier) | Идентификатор стиля, не зависящий от локали. |
| [StyleType](../com.aspose.words/styletype) | Представляет тип стиля. |
| [SubDocument](../com.aspose.words/subdocument) |  Представляет**SubDocument** \- который является ссылкой на внешне сохраненный документ. |
| [SvgSaveOptions](../com.aspose.words/svgsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#SVG](../com.aspose.words/saveformat\#SVG) формат. |
| [SvgTextOutputMode](../com.aspose.words/svgtextoutputmode) |  |
| [SystemFontSource](../com.aspose.words/systemfontsource) | Представляет все шрифты TrueType, установленные в системе. |
| [TabAlignment](../com.aspose.words/tabalignment) | Определяет выравнивание/тип позиции табуляции. |
| [TabLeader](../com.aspose.words/tableader) | Указывает тип линии выноски, отображаемой под символом табуляции. |
| [TabStop](../com.aspose.words/tabstop) | Представляет одну настраиваемую позицию табуляции. |
| [TabStopCollection](../com.aspose.words/tabstopcollection) |  Коллекция[TabStop](../com.aspose.words/tabstop) объекты, представляющие настраиваемые вкладки для абзаца или стиля. |
| [Table](../com.aspose.words/table) | Представляет таблицу в документе Word. |
| [TableAlignment](../com.aspose.words/tablealignment) | Указывает выравнивание для встроенной таблицы. |
| [TableCollection](../com.aspose.words/tablecollection) |  Предоставляет типизированный доступ к коллекции[Table](../com.aspose.words/table) узлы. |
| [TableContentAlignment](../com.aspose.words/tablecontentalignment) | Позволяет указать выравнивание содержимого таблицы, которое будет использоваться при экспорте в формат Markdown. |
| [TableStyle](../com.aspose.words/tablestyle) | Представляет стиль таблицы. |
| [TableStyleOptions](../com.aspose.words/tablestyleoptions) | Указывает, как стиль таблицы применяется к таблице. |
| [TableSubstitutionRule](../com.aspose.words/tablesubstitutionrule) | Правило подстановки табличного шрифта. |
| [TaskPane](../com.aspose.words/taskpane) | Представляет объект области задач надстройки. |
| [TaskPaneCollection](../com.aspose.words/taskpanecollection) | Указывает список сохраняемых объектов области задач. |
| [TaskPaneDockState](../com.aspose.words/taskpanedockstate) | Перечисляет доступные местоположения объекта области задач. |
| [TextBox](../com.aspose.words/textbox) | Определяет атрибуты, определяющие способ отображения текста внутри фигуры. |
| [TextBoxAnchor](../com.aspose.words/textboxanchor) | Указывает значения, используемые для вертикального выравнивания текста фигуры. |
| [TextBoxWrapMode](../com.aspose.words/textboxwrapmode) | Указывает, как текст обтекает фигуру. |
| [TextColumn](../com.aspose.words/textcolumn) | Представляет один текстовый столбец. |
| [TextColumnCollection](../com.aspose.words/textcolumncollection) |  Коллекция[TextColumn](../com.aspose.words/textcolumn) объекты, представляющие все столбцы текста в разделе документа. |
| [TextDmlEffect](../com.aspose.words/textdmleffect) | Текстовый эффект Dml для текстовых прогонов. |
| [TextEffect](../com.aspose.words/texteffect) | Анимационный эффект для текстовых прогонов. |
| [TextFormFieldType](../com.aspose.words/textformfieldtype) | Указывает тип поля текстовой формы. |
| [TextOrientation](../com.aspose.words/textorientation) | Задает ориентацию текста на странице, в ячейке таблицы или текстовом фрейме. |
| [TextPath](../com.aspose.words/textpath) | Определяет текст и форматирование пути к тексту (объекта WordArt). |
| [TextPathAlignment](../com.aspose.words/textpathalignment) | Выравнивание WordArt. |
| [TextWatermarkOptions](../com.aspose.words/textwatermarkoptions) | Содержит параметры, которые можно указать при добавлении водяного знака с текстом. |
| [TextWrapping](../com.aspose.words/textwrapping) | Указывает, как текст обтекает таблицу. |
| [TextureAlignment](../com.aspose.words/texturealignment) | Определяет выравнивание для мозаичного заполнения текстурной заливки. |
| [TextureIndex](../com.aspose.words/textureindex) | Задает текстуру затенения. |
| [Theme](../com.aspose.words/theme) |  Представляет тему документа и обеспечивает доступ к основным частям темы, включая[Theme.\#getMajorFonts()](../com.aspose.words/theme\#getMajorFonts--), [Theme.\#getMinorFonts()](../com.aspose.words/theme\#getMinorFonts--) а также[Theme.\#getColors()](../com.aspose.words/theme\#getColors--) |
| [ThemeColor](../com.aspose.words/themecolor) | Указывает цвета темы для тем документа. |
| [ThemeColors](../com.aspose.words/themecolors) | Представляет цветовую схему темы документа, которая содержит двенадцать цветов. |
| [ThemeFont](../com.aspose.words/themefont) | Указывает типы имен шрифтов темы для тем документа. |
| [ThemeFonts](../com.aspose.words/themefonts) |  Представляет набор шрифтов в схеме шрифтов, что позволяет указывать разные шрифты для разных языков.[ThemeFonts.\#getLatin()](../com.aspose.words/themefonts\#getLatin--) / [ThemeFonts.\#setLatin(java.lang.String)](../com.aspose.words/themefonts\#setLatin-java.lang.String-), [ThemeFonts.\#getEastAsian()](../com.aspose.words/themefonts\#getEastAsian--) / [ThemeFonts.\#setEastAsian(java.lang.String)](../com.aspose.words/themefonts\#setEastAsian-java.lang.String-) а также[ThemeFonts.\#getComplexScript()](../com.aspose.words/themefonts\#getComplexScript--) / [ThemeFonts.\#setComplexScript(java.lang.String)](../com.aspose.words/themefonts\#setComplexScript-java.lang.String-). |
| [ThumbnailGeneratingOptions](../com.aspose.words/thumbnailgeneratingoptions) | Может использоваться для указания дополнительных параметров при создании миниатюры для документа. |
| [TiffCompression](../com.aspose.words/tiffcompression) | Указывает, какой тип сжатия следует применять при сохранении изображений страниц в файл TIFF. |
| [ToaCategories](../com.aspose.words/toacategories) | Представляет таблицу категорий полномочий. |
| [TxtExportHeadersFootersMode](../com.aspose.words/txtexportheadersfootersmode) | Указывает, как верхние и нижние колонтитулы экспортируются в обычный текстовый формат. |
| [TxtLeadingSpacesOptions](../com.aspose.words/txtleadingspacesoptions) |  Определяет доступные параметры для обработки начального пробела во время импорта из[LoadFormat.\#TEXT](../com.aspose.words/loadformat\#TEXT) файл. |
| [TxtListIndentation](../com.aspose.words/txtlistindentation) |  Определяет отступ уровней списка при экспорте документа в[SaveFormat.\#TEXT](../com.aspose.words/saveformat\#TEXT) формат. |
| [TxtLoadOptions](../com.aspose.words/txtloadoptions) |  Позволяет указать дополнительные параметры при загрузке[LoadFormat.\#TEXT](../com.aspose.words/loadformat\#TEXT) документ в[Document](../com.aspose.words/document) объект. |
| [TxtSaveOptions](../com.aspose.words/txtsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#TEXT](../com.aspose.words/saveformat\#TEXT) формат. |
| [TxtSaveOptionsBase](../com.aspose.words/txtsaveoptionsbase) | Базовый класс для указания дополнительных параметров при сохранении документа в текстовые форматы. |
| [TxtTrailingSpacesOptions](../com.aspose.words/txttrailingspacesoptions) |  Указывает доступные параметры обработки конечных пробелов при импорте из[LoadFormat.\#TEXT](../com.aspose.words/loadformat\#TEXT) файл. |
| [Underline](../com.aspose.words/underline) | Указывает тип подчеркивания, примененного к шрифту. |
| [UnicodeScript](../com.aspose.words/unicodescript) |  |
| [UnsupportedFileFormatException](../com.aspose.words/unsupportedfileformatexception) | Возникает во время загрузки документа, когда формат документа не распознается или не поддерживается Aspose.Words. |
| [UserInformation](../com.aspose.words/userinformation) | Указывает информацию о пользователе. |
| [VariableCollection](../com.aspose.words/variablecollection) | Набор переменных документа. |
| [VbaModule](../com.aspose.words/vbamodule) | Предоставляет доступ к модулю проекта VBA. |
| [VbaModuleCollection](../com.aspose.words/vbamodulecollection) |  Представляет собой совокупность[VbaModule](../com.aspose.words/vbamodule) объекты. |
| [VbaModuleType](../com.aspose.words/vbamoduletype) | Указывает тип модели в проекте VBA. |
| [VbaProject](../com.aspose.words/vbaproject) | Предоставляет доступ к информации о проекте VBA. |
| [VbaReference](../com.aspose.words/vbareference) | Реализует ссылку на библиотеку типов автоматизации или проект VBA. |
| [VbaReferenceCollection](../com.aspose.words/vbareferencecollection) |  Представляет собой совокупность[VbaReference](../com.aspose.words/vbareference) объекты. |
| [VbaReferenceType](../com.aspose.words/vbareferencetype) |  Позволяет указать тип[VbaReference](../com.aspose.words/vbareference) объект. |
| [VerticalAlignment](../com.aspose.words/verticalalignment) | Задает вертикальное выравнивание плавающей фигуры, текстового фрейма или плавающей таблицы. |
| [ViewOptions](../com.aspose.words/viewoptions) | Предоставляет различные параметры, управляющие отображением документа в Microsoft Word. |
| [ViewType](../com.aspose.words/viewtype) | Возможные значения режима просмотра в Microsoft Word. |
| [VisitorAction](../com.aspose.words/visitoraction) | Позволяет посетителю контролировать перечисление узлов. |
| [WarningInfo](../com.aspose.words/warninginfo) | Содержит информацию о предупреждении, выданном Aspose.Words при загрузке или сохранении документа. |
| [WarningInfoCollection](../com.aspose.words/warninginfocollection) |  Представляет типизированную коллекцию[WarningInfo](../com.aspose.words/warninginfo) объекты. |
| [WarningSource](../com.aspose.words/warningsource) | Указывает модуль, который выдает предупреждение во время загрузки или сохранения документа. |
| [WarningType](../com.aspose.words/warningtype) | Указывает тип предупреждения, выдаваемого Aspose.Words во время загрузки или сохранения документа. |
| [Watermark](../com.aspose.words/watermark) | Представляет класс для работы с водяным знаком документа. |
| [WatermarkLayout](../com.aspose.words/watermarklayout) | Определяет расположение водяного знака относительно центра водяного знака. |
| [WatermarkType](../com.aspose.words/watermarktype) | Указывает тип водяного знака. |
| [WebExtension](../com.aspose.words/webextension) | Представляет объект веб-расширения. |
| [WebExtensionBinding](../com.aspose.words/webextensionbinding) | Задает отношение привязки между веб-расширением и данными в документе. |
| [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection) | Задает список привязок веб-расширения. |
| [WebExtensionBindingType](../com.aspose.words/webextensionbindingtype) | Перечисляет доступные типы привязки между веб-расширением и данными в документе. |
| [WebExtensionProperty](../com.aspose.words/webextensionproperty) | Указывает настраиваемое свойство веб-расширения. |
| [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection) | Указывает набор настраиваемых свойств веб-расширения. |
| [WebExtensionReference](../com.aspose.words/webextensionreference) | Представляет ссылку на веб-расширение. |
| [WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection) | Задает список ссылок на веб-расширения. |
| [WebExtensionStoreType](../com.aspose.words/webextensionstoretype) | Перечисляет доступные типы магазина веб-расширений. |
| [WordML2003SaveOptions](../com.aspose.words/wordml2003saveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#WORD\_ML](../com.aspose.words/saveformat\#WORD-ML) формат. |
| [WrapSide](../com.aspose.words/wrapside) | Указывает, какую сторону (стороны) фигуры или изображения обтекает текст. |
| [WrapType](../com.aspose.words/wraptype) | Указывает, как текст обтекает фигуру или изображение. |
| [WriteProtection](../com.aspose.words/writeprotection) | Указывает параметры защиты от записи для документа. |
| [X509Certificate2Wrapper](../com.aspose.words/x509certificate2wrapper) |  |
| [XamlFixedSaveOptions](../com.aspose.words/xamlfixedsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#XAML\_FIXED](../com.aspose.words/saveformat\#XAML-FIXED) формат. |
| [XamlFlowSaveOptions](../com.aspose.words/xamlflowsaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#XAML\_FLOW](../com.aspose.words/saveformat\#XAML-FLOW) или же[SaveFormat.\#XAML\_FLOW\_PACK](../com.aspose.words/saveformat\#XAML-FLOW-PACK) формат. |
| [XmlDataLoadOptions](../com.aspose.words/xmldataloadoptions) | Представляет параметры загрузки XML-данных. |
| [XmlDataSource](../com.aspose.words/xmldatasource) | Предоставляет доступ к данным XML-файла или потока для использования в отчете. |
| [XmlMapping](../com.aspose.words/xmlmapping) | Задает информацию, используемую для установления сопоставления между тегом родительского структурированного документа и элементом XML, хранящимся в пользовательской части данных XML в документе. |
| [XpsSaveOptions](../com.aspose.words/xpssaveoptions) |  Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.\#XPS](../com.aspose.words/saveformat\#XPS) формат. |
| [ZoomType](../com.aspose.words/zoomtype) | Возможные значения размера документа, отображаемого на экране в Microsoft Word. |

## Интерфейсы

| Интерфейс | Описание |
| --- | --- |
| [IBarcodeGenerator](../com.aspose.words/ibarcodegenerator) | Публичный интерфейс для пользовательского генератора штрих-кода. |
| [IChartDataPoint](../com.aspose.words/ichartdatapoint) | Содержит свойства одной точки данных на диаграмме. |
| [IComparisonExpressionEvaluator](../com.aspose.words/icomparisonexpressionevaluator) |  При реализации позволяет переопределить оценку выражений сравнения по умолчанию для[FieldIf](../com.aspose.words/fieldif) а также[FieldCompare](../com.aspose.words/fieldcompare) поля. |
| [ICssSavingCallback](../com.aspose.words/icsssavingcallback) | Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет CSS (каскадную таблицу стилей) при сохранении документа в HTML. |
| [IDocumentLoadingCallback](../com.aspose.words/idocumentloadingcallback) | Реализуйте этот интерфейс, если вы хотите, чтобы во время загрузки документа вызывался ваш собственный метод. |
| [IDocumentPartSavingCallback](../com.aspose.words/idocumentpartsavingcallback) |  Реализуйте этот интерфейс, если хотите получать уведомления и управлять тем, как Aspose.Words сохраняет части документа при экспорте документа в[SaveFormat.\#HTML](../com.aspose.words/saveformat\#HTML) или же[SaveFormat.\#EPUB](../com.aspose.words/saveformat\#EPUB) формат. |
| [IDocumentReaderPlugin](../com.aspose.words/idocumentreaderplugin) | Определяет интерфейс для внешних подключаемых модулей чтения, которые могут считывать файл в документ. |
| [IDocumentSavingCallback](../com.aspose.words/idocumentsavingcallback) | Реализуйте этот интерфейс, если вы хотите, чтобы во время сохранения документа вызывался ваш собственный метод. |
| [IFieldDatabaseProvider](../com.aspose.words/ifielddatabaseprovider) |  Реализуйте этот интерфейс для предоставления данных для[FieldDatabase](../com.aspose.words/fielddatabase)поле, когда оно обновляется. |
| [IFieldMergingCallback](../com.aspose.words/ifieldmergingcallback) | Реализуйте этот интерфейс, если вы хотите контролировать, как данные вставляются в поля слияния во время операции слияния. |
| [IFieldResultFormatter](../com.aspose.words/ifieldresultformatter) | Реализуйте этот интерфейс, если хотите управлять форматированием результата поля. |
| [IFieldUpdateCultureProvider](../com.aspose.words/ifieldupdatecultureprovider) |  При реализации обеспечивает[CultureInfo](../com.aspose.words.net.system.globalization/cultureinfo) объект, который следует использовать при обновлении конкретного поля. |
| [IFieldUpdatingCallback](../com.aspose.words/ifieldupdatingcallback) | Реализуйте этот интерфейс, если вы хотите, чтобы во время обновления поля вызывались ваши собственные пользовательские методы. |
| [IFieldUserPromptRespondent](../com.aspose.words/ifielduserpromptrespondent) | Представляет ответчика на запросы пользователя во время обновления поля. |
| [IFontSavingCallback](../com.aspose.words/ifontsavingcallback) | Реализуйте этот интерфейс, если хотите получать уведомления и управлять тем, как Aspose.Words сохраняет шрифты при экспорте документа в формат HTML. |
| [IHyphenationCallback](../com.aspose.words/ihyphenationcallback) | Реализуется классами, которые могут регистрировать словари переносов. |
| [IImageSavingCallback](../com.aspose.words/iimagesavingcallback) | Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет изображения при сохранении документа в HTML. |
| [IMailMergeCallback](../com.aspose.words/imailmergecallback) | Реализуйте этот интерфейс, если хотите получать уведомления во время слияния почты. |
| [IMailMergeDataSource](../com.aspose.words/imailmergedatasource) | Реализуйте этот интерфейс, чтобы разрешить слияние почты из пользовательского источника данных, например списка объектов. |
| [IMailMergeDataSourceRoot](../com.aspose.words/imailmergedatasourceroot) | Реализуйте этот интерфейс, чтобы разрешить слияние почты из пользовательского источника данных с основными и подробными данными. |
| [INodeChangingCallback](../com.aspose.words/inodechangingcallback) | Реализуйте этот интерфейс, если хотите получать уведомления о вставке или удалении узлов в документе. |
| [IPageLayoutCallback](../com.aspose.words/ipagelayoutcallback) | Реализуйте этот интерфейс, если вы хотите, чтобы во время сборки и рендеринга модели макета страницы вызывался собственный пользовательский метод. |
| [IPageSavingCallback](../com.aspose.words/ipagesavingcallback) | Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет отдельные страницы при сохранении документа в фиксированных форматах страниц. |
| [IReplacingCallback](../com.aspose.words/ireplacingcallback) | Реализуйте этот интерфейс, если вы хотите, чтобы во время операции поиска и замены вызывался ваш собственный метод. |
| [IResourceLoadingCallback](../com.aspose.words/iresourceloadingcallback) |  Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words загружает внешний ресурс при импорте документа и вставке изображений с помощью[DocumentBuilder](../com.aspose.words/documentbuilder). |
| [IResourceSavingCallback](../com.aspose.words/iresourcesavingcallback) | Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет внешние ресурсы (изображения, шрифты и css) при сохранении документа на фиксированную страницу HTML или SVG. |
| [IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag) |  Интерфейс для определения общих данных для[StructuredDocumentTag](../com.aspose.words/structureddocumenttag) а также[StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart). |
| [ITextShaper](../com.aspose.words/itextshaper) |  |
| [ITextShaperFactory](../com.aspose.words/itextshaperfactory) |  |
| [IWarningCallback](../com.aspose.words/iwarningcallback) | Реализуйте этот интерфейс, если вы хотите, чтобы ваш собственный метод вызывался для сбора предупреждений о потере точности, которые могут возникнуть во время загрузки или сохранения документа. |