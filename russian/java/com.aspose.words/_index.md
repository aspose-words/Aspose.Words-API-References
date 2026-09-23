---
title: "com.aspose.words"
linktitle: "com.aspose.words"
second_title: "Aspose.Words для Java"
description: "Пакет com.aspose.words предоставляет классы для создания, конвертации, изменения, визуализации и печати документов Microsoft Word без использования Microsoft Word в Java."
type: docs
weight: 10
url: /ru/java/com.aspose.words/
---


Пакет **com.aspose.words** предоставляет классы для создания, конвертации, изменения, визуализации и печати документов Microsoft Word без использования Microsoft Word.

Aspose.Words полностью написан на Java. Microsoft Word не требуется для использования Aspose.Words.

Классы в пакете **com.aspose.words** заимствуют лучшие практики из двух известных фреймворков: Microsoft Word Automation и System.Xml. Документ в Aspose.Words представляется в виде дерева узлов, аналогично XML DOM. По возможности имена классов, методов и свойств совпадают с теми, что используются в Microsoft Word Automation.

Основные классы в этом пространстве имён:

 *  **Document** is the main class of the object model that represents a Microsoft Word document.
 *  **DocumentBuilder** provides an easy way to insert content and formatting into a document.
 *  **Node** is the base class for all nodes in the document.
 *  **CompositeNode** is the base class for all nodes of the document that can contain other nodes, for example **Paragraph**, **Section** and **Table** and .

Пакет **com.aspose.words** также содержит классы, формирующие движок отчётности Aspose.Words. Движок отчётности позволяет быстро и легко заполнять документы, созданные в Microsoft Word, данными из различных источников, таких как **java.sql.ResultSet**, **array of ResultSets**, **com.aspose.words.net.System.Data.DataSet** или **array of values**.

Объект **MailMerge**, предоставляющий доступ к функционалу отчётности, доступен через свойство **Document.MailMerge**.


## Классы

| Класс | Описание |
| --- | --- |
| [AbsolutePositionTab](../com.aspose.words/absolutepositiontab/) | Табуляция абсолютной позиции — это символ, используемый для перемещения позиции на текущей строке текста при отображении этого содержимого WordprocessingML. |
| [Adjustment](../com.aspose.words/adjustment/) | Представляет значения корректировок, применяемые к указанной фигуре. |
| [AdjustmentCollection](../com.aspose.words/adjustmentcollection/) | Представляет только для чтения коллекцию [Adjustment](../com.aspose.words/adjustment/) значений корректировок, применяемых к указанной фигуре. |
| [AdvancedCompareOptions](../com.aspose.words/advancedcompareoptions/) | Позволяет задавать расширенные параметры сравнения. |
| [AiModel](../com.aspose.words/aimodel/) | Абстрактный класс, представляющий интеграцию с различными моделями ИИ в Aspose.Words. |
| [AiModelType](../com.aspose.words/aimodeltype/) | Представляет типы [AiModel](../com.aspose.words/aimodel/), которые могут быть интегрированы в процесс обработки документов. |
| [AnthropicAiModel](../com.aspose.words/anthropicaimodel/) | Абстрактный класс, представляющий интеграцию с AI‑моделями Anthropic в Aspose.Words. |
| [ArrowLength](../com.aspose.words/arrowlength/) | Длина стрелки в конце линии. |
| [ArrowType](../com.aspose.words/arrowtype/) | Указывает тип стрелки в конце линии. |
| [ArrowWidth](../com.aspose.words/arrowwidth/) | Ширина стрелки в конце линии. |
| [AsposeWordsPrintDocument](../com.aspose.words/asposewordsprintdocument/) | Предоставляет реализацию по умолчанию для печати [Document](../com.aspose.words/document/) в рамках Java‑печати. |
| [AutoFitBehavior](../com.aspose.words/autofitbehavior/) | Определяет, как Aspose.Words изменяет размер таблицы при вызове метода **M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**. |
| [AxisBound](../com.aspose.words/axisbound/) | Представляет минимальную или максимальную границу значений оси. |
| [AxisBuiltInUnit](../com.aspose.words/axisbuiltinunit/) | Указывает единицы отображения для оси. |
| [AxisCategoryType](../com.aspose.words/axiscategorytype/) | Указывает тип категориальной оси. |
| [AxisCrosses](../com.aspose.words/axiscrosses/) | Указывает возможные точки пересечения оси. |
| [AxisDisplayUnit](../com.aspose.words/axisdisplayunit/) | Предоставляет доступ к параметрам масштабирования единиц отображения для оси значений. |
| [AxisGroup](../com.aspose.words/axisgroup/) | Представляет тип группы осей диаграммы. |
| [AxisScaleType](../com.aspose.words/axisscaletype/) | Указывает возможные типы шкалы для оси. |
| [AxisScaling](../com.aspose.words/axisscaling/) | Представляет параметры масштабирования оси. |
| [AxisTickLabelPosition](../com.aspose.words/axisticklabelposition/) | Указывает возможные положения меток делений. |
| [AxisTickLabels](../com.aspose.words/axisticklabels/) | Представляет свойства меток делений оси. |
| [AxisTickMark](../com.aspose.words/axistickmark/) | Указывает возможные положения делений. |
| [AxisTimeUnit](../com.aspose.words/axistimeunit/) | Указывает единицу времени для осей. |
| [BarcodeParameters](../com.aspose.words/barcodeparameters/) | Класс‑контейнер для параметров штрихкода, передаваемых в BarcodeGenerator. |
| [BaseWebExtensionCollection](../com.aspose.words/basewebextensioncollection/) | Базовый класс для коллекций [TaskPaneCollection](../com.aspose.words/taskpanecollection/), [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection/), [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection/) и [WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection/). |
| [BaselineAlignment](../com.aspose.words/baselinealignment/) | Указывает вертикальное положение шрифтов в строке. |
| [BasicTextShaperCache](../com.aspose.words/basictextshapercache/) | Реализует базовый кэш для экземпляров [ITextShaper](../com.aspose.words/itextshaper/). |
| [Bibliography](../com.aspose.words/bibliography/) | Представляет список источников библиографии, доступных в документе. |
| [BlockImportMode](../com.aspose.words/blockimportmode/) | Указывает, как свойства блочных элементов импортируются из HTML‑документов. |
| [Body](../com.aspose.words/body/) | Представляет контейнер для основного текста раздела. |
| [Bookmark](../com.aspose.words/bookmark/) | Представляет одну закладку. |
| [BookmarkCollection](../com.aspose.words/bookmarkcollection/) | Коллекция объектов [Bookmark](../com.aspose.words/bookmark/), представляющих закладки в указанном диапазоне. |
| [BookmarkEnd](../com.aspose.words/bookmarkend/) | Представляет конец закладки в документе Word. |
| [BookmarkStart](../com.aspose.words/bookmarkstart/) | Представляет начало закладки в документе Word. |
| [BookmarksOutlineLevelCollection](../com.aspose.words/bookmarksoutlinelevelcollection/) | Коллекция отдельных уровней структуры закладок. |
| [Border](../com.aspose.words/border/) | Представляет границу объекта. |
| [BorderCollection](../com.aspose.words/bordercollection/) | Коллекция объектов [Border](../com.aspose.words/border/). |
| [BorderType](../com.aspose.words/bordertype/) | Указывает стороны границы. |
| [BreakType](../com.aspose.words/breaktype/) | Указывает тип разрыва внутри документа. |
| [BubbleSizeCollection](../com.aspose.words/bubblesizecollection/) | Представляет коллекцию размеров пузырей для серии диаграммы. |
| [BuildVersionInfo](../com.aspose.words/buildversioninfo/) | Предоставляет информацию о текущем названии продукта и его версии. |
| [BuildingBlock](../com.aspose.words/buildingblock/) | Представляет запись глоссария документа, такую как Building Block, AutoText или запись AutoCorrect. |
| [BuildingBlockBehavior](../com.aspose.words/buildingblockbehavior/) | Указывает поведение, которое будет применено к содержимому строительного блока при его вставке в основной документ. |
| [BuildingBlockCollection](../com.aspose.words/buildingblockcollection/) | Коллекция объектов [BuildingBlock](../com.aspose.words/buildingblock/) в документе. |
| [BuildingBlockGallery](../com.aspose.words/buildingblockgallery/) | Указывает предопределённую галерею, в которую классифицируется строительный блок. |
| [BuildingBlockType](../com.aspose.words/buildingblocktype/) | Указывает тип строительного блока. |
| [BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties/) | Коллекция встроенных свойств документа. |
| [CalendarType](../com.aspose.words/calendartype/) | Указывает тип календаря. |
| [Cell](../com.aspose.words/cell/) | Представляет ячейку таблицы. |
| [CellCollection](../com.aspose.words/cellcollection/) | Обеспечивает типизированный доступ к коллекции узлов [Cell](../com.aspose.words/cell/). |
| [CellFormat](../com.aspose.words/cellformat/) | Представляет всё форматирование ячейки таблицы. |
| [CellMerge](../com.aspose.words/cellmerge/) | Указывает, как ячейка в таблице объединяется с другими ячейками. |
| [CellVerticalAlignment](../com.aspose.words/cellverticalalignment/) | Указывает вертикальное выравнивание текста внутри ячейки таблицы. |
| [CertificateHolder](../com.aspose.words/certificateholder/) | Представляет контейнер экземпляра **X509Certificate2**. |
| [ChapterPageSeparator](../com.aspose.words/chapterpageseparator/) | Определяет символ-разделитель, который появляется между номером главы и номером страницы. |
| [Chart](../com.aspose.words/chart/) | Предоставляет доступ к свойствам формы диаграммы. |
| [ChartAxis](../com.aspose.words/chartaxis/) | Представляет параметры оси диаграммы. |
| [ChartAxisCollection](../com.aspose.words/chartaxiscollection/) | Представляет коллекцию осей диаграммы. |
| [ChartAxisTitle](../com.aspose.words/chartaxistitle/) | Предоставляет доступ к свойствам заголовка оси. |
| [ChartAxisType](../com.aspose.words/chartaxistype/) | Указывает тип оси диаграммы. |
| [ChartDataLabel](../com.aspose.words/chartdatalabel/) | Представляет подпись данных на точке диаграммы или линии тренда. |
| [ChartDataLabelCollection](../com.aspose.words/chartdatalabelcollection/) | Представляет коллекцию [ChartDataLabel](../com.aspose.words/chartdatalabel/). |
| [ChartDataLabelLocationMode](../com.aspose.words/chartdatalabellocationmode/) | Указывает, как значения \\u200b\\u200b, определяющие расположение подписи данных — свойства [ChartDataLabel.#getLeft()](../com.aspose.words/chartdatalabel/#getLeft) / [ChartDataLabel.#setLeft(double)](../com.aspose.words/chartdatalabel/#setLeft-double) и [ChartDataLabel.#getTop()](../com.aspose.words/chartdatalabel/#getTop) / [ChartDataLabel.#setTop(double)](../com.aspose.words/chartdatalabel/#setTop-double) — интерпретируются. |
| [ChartDataLabelPosition](../com.aspose.words/chartdatalabelposition/) | Указывает позицию подписи данных диаграммы. |
| [ChartDataPoint](../com.aspose.words/chartdatapoint/) | Позволяет указать форматирование отдельной точки данных на диаграмме. |
| [ChartDataPointCollection](../com.aspose.words/chartdatapointcollection/) | Представляет коллекцию [ChartDataPoint](../com.aspose.words/chartdatapoint/). |
| [ChartDataTable](../com.aspose.words/chartdatatable/) | Позволяет указать свойства таблицы данных диаграммы. |
| [ChartFormat](../com.aspose.words/chartformat/) | Представляет форматирование элемента диаграммы. |
| [ChartLegend](../com.aspose.words/chartlegend/) | Представляет свойства легенды диаграммы. |
| [ChartLegendEntry](../com.aspose.words/chartlegendentry/) | Представляет запись легенды диаграммы. |
| [ChartLegendEntryCollection](../com.aspose.words/chartlegendentrycollection/) | Представляет коллекцию записей легенды диаграммы. |
| [ChartMarker](../com.aspose.words/chartmarker/) | Представляет маркер данных диаграммы. |
| [ChartMultilevelValue](../com.aspose.words/chartmultilevelvalue/) | Представляет значение для диаграмм, отображающих многоуровневые данные. |
| [ChartNumberFormat](../com.aspose.words/chartnumberformat/) | Представляет числовое форматирование родительского элемента. |
| [ChartSeries](../com.aspose.words/chartseries/) | Представляет свойства серии диаграммы. |
| [ChartSeriesCollection](../com.aspose.words/chartseriescollection/) | Представляет коллекцию [ChartSeries](../com.aspose.words/chartseries/). |
| [ChartSeriesGroup](../com.aspose.words/chartseriesgroup/) | Представляет свойства группы серий диаграммы, то есть свойства серий диаграммы одного типа, связанных с одними и теми же осями. |
| [ChartSeriesGroupCollection](../com.aspose.words/chartseriesgroupcollection/) | Представляет коллекцию объектов [ChartSeriesGroup](../com.aspose.words/chartseriesgroup/). |
| [ChartSeriesType](../com.aspose.words/chartseriestype/) | Указывает тип серии диаграммы. |
| [ChartShapeType](../com.aspose.words/chartshapetype/) | Указывает тип формы элементов диаграммы. |
| [ChartStyle](../com.aspose.words/chartstyle/) | Указывает предопределённые стили диаграммы. |
| [ChartTitle](../com.aspose.words/charttitle/) | Предоставляет доступ к свойствам заголовка диаграммы. |
| [ChartType](../com.aspose.words/charttype/) | Указывает тип диаграммы. |
| [ChartXValue](../com.aspose.words/chartxvalue/) | Представляет значение X для серии диаграммы. |
| [ChartXValueCollection](../com.aspose.words/chartxvaluecollection/) | Представляет коллекцию значений X для серии диаграммы. |
| [ChartXValueType](../com.aspose.words/chartxvaluetype/) | Позволяет указать тип значения X серии диаграммы. |
| [ChartYValue](../com.aspose.words/chartyvalue/) | Представляет значение Y для серии диаграммы. |
| [ChartYValueCollection](../com.aspose.words/chartyvaluecollection/) | Представляет коллекцию значений Y для серии диаграммы. |
| [ChartYValueType](../com.aspose.words/chartyvaluetype/) | Позволяет указать тип значения Y серии диаграммы. |
| [CheckBoxControl](../com.aspose.words/checkboxcontrol/) | Элемент управления CheckBox переключает значение. |
| [CheckGrammarOptions](../com.aspose.words/checkgrammaroptions/) | Позволяет указать различные параметры при проверке грамматики документа с использованием ИИ. |
| [ChmLoadOptions](../com.aspose.words/chmloadoptions/) | Позволяет указать дополнительные параметры при загрузке CHM‑документа в объект [Document](../com.aspose.words/document/) . |
| [CleanupOptions](../com.aspose.words/cleanupoptions/) | Позволяет указать параметры очистки документа. |
| [Cluster](../com.aspose.words/cluster/) | Инкапсулирует кодовые точки и глифы, составляющие графему. |
| [ColorMode](../com.aspose.words/colormode/) | Указывает, как отображаются цвета. |
| [ColorPrintMode](../com.aspose.words/colorprintmode/) | Указывает, как печатаются бесцветные страницы, если устройство поддерживает цветную печать. |
| [CommandButtonControl](../com.aspose.words/commandbuttoncontrol/) | Элемент управления CommandButton запускает макрос, выполняющий действие при щелчке пользователя. |
| [Comment](../com.aspose.words/comment/) | Представляет контейнер для текста комментария. |
| [CommentCollection](../com.aspose.words/commentcollection/) | Предоставляет типизированный доступ к коллекции узлов [Comment](../com.aspose.words/comment/). |
| [CommentDisplayMode](../com.aspose.words/commentdisplaymode/) | Указывает режим отображения комментариев документа. |
| [CommentRangeEnd](../com.aspose.words/commentrangeend/) | Обозначает конец области текста, к которой привязан комментарий. |
| [CommentRangeStart](../com.aspose.words/commentrangestart/) | Обозначает начало области текста, к которой привязан комментарий. |
| [CompareOptions](../com.aspose.words/compareoptions/) | Позволяет выбрать дополнительные параметры для операции сравнения документов. |
| [Comparer](../com.aspose.words/comparer/) | Предоставляет методы, предназначенные для сравнения документов. |
| [ComparerContext](../com.aspose.words/comparercontext/) | Контекст сравнения документов |
| [ComparisonEvaluationResult](../com.aspose.words/comparisonevaluationresult/) | Результат оценки сравнения. |
| [ComparisonExpression](../com.aspose.words/comparisonexpression/) | Выражение сравнения. |
| [ComparisonTargetType](../com.aspose.words/comparisontargettype/) | Позволяет указать базовый документ, который будет использоваться во время сравнения. |
| [Compatibility](../com.aspose.words/compatibility/) | Указывает имена параметров совместимости. |
| [CompatibilityOptions](../com.aspose.words/compatibilityoptions/) | Содержит параметры совместимости (то есть пользовательские настройки, введённые на вкладке **Compatibility** диалогового окна **Options** в Microsoft Word). |
| [CompositeNode](../com.aspose.words/compositenode/) | Базовый класс для узлов, которые могут содержать другие узлы. |
| [CompressionLevel](../com.aspose.words/compressionlevel/) | Уровень сжатия для файлов OOXML и XPS. |
| [ConditionalStyle](../com.aspose.words/conditionalstyle/) | Представляет специальное форматирование, применённое к некоторой области таблицы с назначенным стилем таблицы. |
| [ConditionalStyleCollection](../com.aspose.words/conditionalstylecollection/) | Представляет коллекцию объектов [ConditionalStyle](../com.aspose.words/conditionalstyle/). |
| [ConditionalStyleType](../com.aspose.words/conditionalstyletype/) | Представляет возможные области таблицы, к которым может быть определено условное форматирование в стиле таблицы. |
| [ContentDisposition](../com.aspose.words/contentdisposition/) | Перечисляет различные способы отображения документа в браузере клиента. |
| [ContinuousSectionRestart](../com.aspose.words/continuoussectionrestart/) | Представляет различные поведения при вычислении номеров страниц в непрерывном разделе, который перезапускает нумерацию страниц. |
| [Contributor](../com.aspose.words/contributor/) | Представляет участника источника библиографии. |
| [ContributorCollection](../com.aspose.words/contributorcollection/) | Представляет участников источника библиографии. |
| [ControlChar](../com.aspose.words/controlchar/) | Управляющие символы, часто встречающиеся в документах. |
| [ConvertUtil](../com.aspose.words/convertutil/) | Предоставляет вспомогательные функции для преобразования между различными единицами измерения. |
| [Converter](../com.aspose.words/converter/) | Представляет группу методов, предназначенных для конвертации различных типов документов с помощью одной строки кода. |
| [ConverterContext](../com.aspose.words/convertercontext/) | Контекст конвертера документов |
| [Corporate](../com.aspose.words/corporate/) | Представляет корпоративного (организационного) участника источника библиографии. |
| [CssSavingArgs](../com.aspose.words/csssavingargs/) | Предоставляет данные для события [ICssSavingCallback.#cssSaving(com.aspose.words.CssSavingArgs)](../com.aspose.words/icsssavingcallback/#cssSaving-com.aspose.words.CssSavingArgs). |
| [CssStyleSheetType](../com.aspose.words/cssstylesheettype/) | Указывает, как стили CSS (Cascading Style Sheet) экспортируются в HTML. |
| [CsvDataLoadOptions](../com.aspose.words/csvdataloadoptions/) | Представляет параметры для разбора CSV-данных. |
| [CsvDataSource](../com.aspose.words/csvdatasource/) | Обеспечивает доступ к данным CSV‑файла или потока, которые будут использоваться в отчёте. |
| [CurrentThreadSettings](../com.aspose.words/currentthreadsettings/) | Этот класс помогает установить изолированные от потоков локаль и часовой пояс для приложения Aspose.Words. |
| [CustomDocumentProperties](../com.aspose.words/customdocumentproperties/) | Коллекция пользовательских свойств документа. |
| [CustomPart](../com.aspose.words/custompart/) | Представляет пользовательскую (произвольного содержания) часть, которая не определена стандартом ISO/IEC 29500. |
| [CustomPartCollection](../com.aspose.words/custompartcollection/) | Представляет коллекцию объектов [CustomPart](../com.aspose.words/custompart/). |
| [CustomXmlPart](../com.aspose.words/customxmlpart/) | Представляет часть хранилища пользовательских XML‑данных (пользовательские XML‑данные внутри пакета). |
| [CustomXmlPartCollection](../com.aspose.words/customxmlpartcollection/) | Представляет коллекцию пользовательских XML‑частей. |
| [CustomXmlProperty](../com.aspose.words/customxmlproperty/) | Представляет отдельный пользовательский XML‑атрибут или свойство смарт‑тега. |
| [CustomXmlPropertyCollection](../com.aspose.words/customxmlpropertycollection/) | Представляет коллекцию пользовательских XML‑атрибутов или свойств смарт‑тегов. |
| [CustomXmlSchemaCollection](../com.aspose.words/customxmlschemacollection/) | Коллекция строк, представляющих XML‑схемы, связанные с пользовательской XML‑частью. |
| [DashStyle](../com.aspose.words/dashstyle/) | Стиль пунктирной линии. |
| [DefaultFontSubstitutionRule](../com.aspose.words/defaultfontsubstitutionrule/) | Правило замены шрифта по умолчанию. |
| [DigitalSignature](../com.aspose.words/digitalsignature/) | Представляет цифровую подпись документа и результат её проверки. |
| [DigitalSignatureCollection](../com.aspose.words/digitalsignaturecollection/) | Предоставляет только для чтения коллекцию цифровых подписей, прикреплённых к документу. |
| [DigitalSignatureDetails](../com.aspose.words/digitalsignaturedetails/) | Содержит детали подписи документа цифровой подписью. |
| [DigitalSignatureType](../com.aspose.words/digitalsignaturetype/) | Указывает тип цифровой подписи. |
| [DigitalSignatureUtil](../com.aspose.words/digitalsignatureutil/) | Предоставляет методы подписи документа. |
| [Direction](../com.aspose.words/direction/) | Направление текста. |
| [Dml3DEffectsRenderingMode](../com.aspose.words/dml3deffectsrenderingmode/) | Указывает, как отображаются эффекты 3D‑форм. |
| [DmlEffectsRenderingMode](../com.aspose.words/dmleffectsrenderingmode/) | Указывает, как эффекты DrawingML отображаются в фиксированных форматах страниц. |
| [DmlRenderingMode](../com.aspose.words/dmlrenderingmode/) | Указывает, как формы DrawingML отображаются в фиксированных форматах страниц. |
| [DocSaveOptions](../com.aspose.words/docsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\\#DOC](../com.aspose.words/saveformat/\\#DOC) или [SaveFormat.\\#DOT](../com.aspose.words/saveformat/\\#DOT). |
| [DoclingSaveOptions](../com.aspose.words/doclingsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\\#DOCLING](../com.aspose.words/saveformat/\\#DOCLING). |
| [Document](../com.aspose.words/document/) | Представляет документ Word. |
| [DocumentBase](../com.aspose.words/documentbase/) | Предоставляет абстрактный базовый класс для основного документа и глоссария документа Word. |
| [DocumentBuilder](../com.aspose.words/documentbuilder/) | Предоставляет методы вставки текста, изображений и другого содержимого, указания шрифта, форматирования абзацев и разделов. |
| [DocumentBuilderOptions](../com.aspose.words/documentbuilderoptions/) | Позволяет указать дополнительные параметры процесса построения документа. |
| [DocumentDirection](../com.aspose.words/documentdirection/) | Позволяет указать направление потока текста в документе. |
| [DocumentLoadingArgs](../com.aspose.words/documentloadingargs/) | Аргумент, передаваемый в [IDocumentLoadingCallback.\#notify(com.aspose.words.DocumentLoadingArgs)](../com.aspose.words/idocumentloadingcallback/\#notify-com.aspose.words.DocumentLoadingArgs). |
| [DocumentPartSavingArgs](../com.aspose.words/documentpartsavingargs/) | Предоставляет данные для обратного вызова [IDocumentPartSavingCallback.\#documentPartSaving(com.aspose.words.DocumentPartSavingArgs)](../com.aspose.words/idocumentpartsavingcallback/\#documentPartSaving-com.aspose.words.DocumentPartSavingArgs). |
| [DocumentProperty](../com.aspose.words/documentproperty/) | Представляет пользовательское или встроенное свойство документа. |
| [DocumentPropertyCollection](../com.aspose.words/documentpropertycollection/) | Базовый класс для коллекций [BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties/) и [CustomDocumentProperties](../com.aspose.words/customdocumentproperties/). |
| [DocumentReaderPluginLoadException](../com.aspose.words/documentreaderpluginloadexception/) | Выбрасывается при загрузке документа, когда плагин, необходимый для чтения формата документа, не может быть загружен. |
| [DocumentRecoveryMode](../com.aspose.words/documentrecoverymode/) | Указывает доступные варианты восстановления, когда документ сталкивается с ошибками во время загрузки. |
| [DocumentSavingArgs](../com.aspose.words/documentsavingargs/) | Аргумент, передаваемый в [IDocumentSavingCallback.\#notify(com.aspose.words.DocumentSavingArgs)](../com.aspose.words/idocumentsavingcallback/\#notify-com.aspose.words.DocumentSavingArgs). |
| [DocumentSecurity](../com.aspose.words/documentsecurity/) | Используется в качестве значения свойства [BuiltInDocumentProperties.\#getSecurity()](../com.aspose.words/builtindocumentproperties/\#getSecurity) / [BuiltInDocumentProperties.\#setSecurity(int)](../com.aspose.words/builtindocumentproperties/\#setSecurity-int). |
| [DocumentSplitCriteria](../com.aspose.words/documentsplitcriteria/) | Указывает, как документ разбивается на части при сохранении в формат [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB) или [SaveFormat.\#AZW\_3](../com.aspose.words/saveformat/\#AZW-3). |
| [DocumentVisitor](../com.aspose.words/documentvisitor/) | Базовый класс для пользовательских посетителей документа. |
| [DownsampleOptions](../com.aspose.words/downsampleoptions/) | Позволяет указать параметры понижения дискретизации. |
| [DropCapPosition](../com.aspose.words/dropcapposition/) | Указывает позицию текста буквицы. |
| [DropDownItemCollection](../com.aspose.words/dropdownitemcollection/) | Коллекция строк, представляющих все элементы выпадающего поля формы. |
| [EditableRange](../com.aspose.words/editablerange/) | Представляет один редактируемый диапазон. |
| [EditableRangeEnd](../com.aspose.words/editablerangeend/) | Представляет конец редактируемого диапазона в документе Word. |
| [EditableRangeStart](../com.aspose.words/editablerangestart/) | Представляет начало редактируемого диапазона в документе Word. |
| [EditingLanguage](../com.aspose.words/editinglanguage/) | Указывает язык редактирования. |
| [EditorType](../com.aspose.words/editortype/) | Указывает набор возможных псевдонимов (или групп редактирования), которые могут использоваться в качестве псевдонимов для определения, разрешено ли текущему пользователю редактировать отдельный диапазон, определённый редактируемым диапазоном в документе. |
| [EmbeddedFontFormat](../com.aspose.words/embeddedfontformat/) | Указывает формат конкретного встроенного шрифта внутри объекта [FontInfo](../com.aspose.words/fontinfo/). |
| [EmbeddedFontStyle](../com.aspose.words/embeddedfontstyle/) | Указывает стиль встроенного шрифта внутри объекта [FontInfo](../com.aspose.words/fontinfo/). |
| [EmfPlusDualRenderingMode](../com.aspose.words/emfplusdualrenderingmode/) | Указывает, как Aspose.Words должен отображать двойные метафайлы EMF+. |
| [EmphasisMark](../com.aspose.words/emphasismark/) | Указывает возможные типы знаков акцента. |
| [EndCap](../com.aspose.words/endcap/) | Указывает стиль окончания линии. |
| [EndnoteOptions](../com.aspose.words/endnoteoptions/) | Представляет параметры нумерации сносок в документе или разделе. |
| [EndnotePosition](../com.aspose.words/endnoteposition/) | Определяет позицию сноски. |
| [ExportFontFormat](../com.aspose.words/exportfontformat/) | Указывает формат, используемый для экспорта шрифтов при рендеринге в фиксированный формат HTML. |
| [ExportHeadersFootersMode](../com.aspose.words/exportheadersfootersmode/) | Указывает, как заголовки и колонтитулы экспортируются в HTML, MHTML или EPUB. |
| [ExportListLabels](../com.aspose.words/exportlistlabels/) | Указывает, как метки списков экспортируются в HTML, MHTML и EPUB. |
| [Field](../com.aspose.words/field/) | Представляет поле документа Microsoft Word. |
| [FieldAddIn](../com.aspose.words/fieldaddin/) | Реализует поле ADDIN. |
| [FieldAddressBlock](../com.aspose.words/fieldaddressblock/) | Реализует поле ADDRESSBLOCK. |
| [FieldAdvance](../com.aspose.words/fieldadvance/) | Реализует поле ADVANCE. |
| [FieldArgumentBuilder](../com.aspose.words/fieldargumentbuilder/) | Создаёт сложный аргумент поля, состоящий из полей, узлов и обычного текста. |
| [FieldAsk](../com.aspose.words/fieldask/) | Реализует поле ASK. |
| [FieldAuthor](../com.aspose.words/fieldauthor/) | Реализует поле AUTHOR. |
| [FieldAutoNum](../com.aspose.words/fieldautonum/) | Реализует поле AUTONUM. |
| [FieldAutoNumLgl](../com.aspose.words/fieldautonumlgl/) | Реализует поле AUTONUMLGL. |
| [FieldAutoNumOut](../com.aspose.words/fieldautonumout/) | Реализует поле AUTONUMOUT. |
| [FieldAutoText](../com.aspose.words/fieldautotext/) | Реализует поле AUTOTEXT. |
| [FieldAutoTextList](../com.aspose.words/fieldautotextlist/) | Реализует поле AUTOTEXTLIST. |
| [FieldBarcode](../com.aspose.words/fieldbarcode/) | Реализует поле BARCODE. |
| [FieldBibliography](../com.aspose.words/fieldbibliography/) | Реализует поле BIBLIOGRAPHY. |
| [FieldBidiOutline](../com.aspose.words/fieldbidioutline/) | Реализует поле BIDIOUTLINE. |
| [FieldBuilder](../com.aspose.words/fieldbuilder/) | Создаёт поле из токенов кода поля (аргументы и переключатели). |
| [FieldChar](../com.aspose.words/fieldchar/) | Базовый класс для узлов, представляющих символы полей в документе. |
| [FieldCitation](../com.aspose.words/fieldcitation/) | Реализует поле CITATION. |
| [FieldCollection](../com.aspose.words/fieldcollection/) | Коллекция объектов [Field](../com.aspose.words/field/), представляющая поля в указанном диапазоне. |
| [FieldComments](../com.aspose.words/fieldcomments/) | Реализует поле COMMENTS. |
| [FieldCompare](../com.aspose.words/fieldcompare/) | Реализует поле COMPARE. |
| [FieldCreateDate](../com.aspose.words/fieldcreatedate/) | Реализует поле CREATEDATE. |
| [FieldData](../com.aspose.words/fielddata/) | Реализует поле DATA. |
| [FieldDatabase](../com.aspose.words/fielddatabase/) | Реализует поле DATABASE. |
| [FieldDatabaseDataRow](../com.aspose.words/fielddatabasedatarow/) | Предоставляет данные для результата поля [FieldDatabase](../com.aspose.words/fielddatabase/). |
| [FieldDatabaseDataTable](../com.aspose.words/fielddatabasedatatable/) | Предоставляет данные для результата поля [FieldDatabase](../com.aspose.words/fielddatabase/). |
| [FieldDate](../com.aspose.words/fielddate/) | Реализует поле DATE. |
| [FieldDde](../com.aspose.words/fielddde/) | Реализует поле DDE. |
| [FieldDdeAuto](../com.aspose.words/fieldddeauto/) | Реализует поле DDEAUTO. |
| [FieldDisplayBarcode](../com.aspose.words/fielddisplaybarcode/) | Реализует поле DISPLAYBARCODE. |
| [FieldDocProperty](../com.aspose.words/fielddocproperty/) | Реализует поле DOCPROPERTY. |
| [FieldDocVariable](../com.aspose.words/fielddocvariable/) | Реализует поле DOCVARIABLE. |
| [FieldEQ](../com.aspose.words/fieldeq/) | Реализует поле EQ. |
| [FieldEditTime](../com.aspose.words/fieldedittime/) | Реализует поле EDITTIME. |
| [FieldEmbed](../com.aspose.words/fieldembed/) | Реализует поле EMBED. |
| [FieldEnd](../com.aspose.words/fieldend/) | Представляет конец поля Word в документе. |
| [FieldFileName](../com.aspose.words/fieldfilename/) | Реализует поле FILENAME. |
| [FieldFileSize](../com.aspose.words/fieldfilesize/) | Реализует поле FILESIZE. |
| [FieldFillIn](../com.aspose.words/fieldfillin/) | Реализует поле FILLIN. |
| [FieldFootnoteRef](../com.aspose.words/fieldfootnoteref/) | Реализует поле FOOTNOTEREF. |
| [FieldFormCheckBox](../com.aspose.words/fieldformcheckbox/) | Реализует поле FORMCHECKBOX. |
| [FieldFormDropDown](../com.aspose.words/fieldformdropdown/) | Реализует поле FORMDROPDOWN. |
| [FieldFormText](../com.aspose.words/fieldformtext/) | Реализует поле FORMTEXT. |
| [FieldFormat](../com.aspose.words/fieldformat/) | Предоставляет типизированный доступ к числовому, датному и временному, а также общему форматированию поля. |
| [FieldFormula](../com.aspose.words/fieldformula/) | Реализует поле = (формула). |
| [FieldGlossary](../com.aspose.words/fieldglossary/) | Реализует поле GLOSSARY. |
| [FieldGoToButton](../com.aspose.words/fieldgotobutton/) | Реализует поле GOTOBUTTON. |
| [FieldGreetingLine](../com.aspose.words/fieldgreetingline/) | Реализует поле GREETINGLINE. |
| [FieldHyperlink](../com.aspose.words/fieldhyperlink/) | Реализует поле HYPERLINK |
| [FieldIf](../com.aspose.words/fieldif/) | Реализует поле IF. |
| [FieldIfComparisonResult](../com.aspose.words/fieldifcomparisonresult/) | Указывает результат оценки условия поля IF. |
| [FieldImport](../com.aspose.words/fieldimport/) | Реализует поле IMPORT. |
| [FieldInclude](../com.aspose.words/fieldinclude/) | Реализует поле INCLUDE. |
| [FieldIncludePicture](../com.aspose.words/fieldincludepicture/) | Реализует поле INCLUDEPICTURE. |
| [FieldIncludeText](../com.aspose.words/fieldincludetext/) | Реализует поле INCLUDETEXT. |
| [FieldIndex](../com.aspose.words/fieldindex/) | Реализует поле INDEX. |
| [FieldIndexFormat](../com.aspose.words/fieldindexformat/) | Указывает форматирование полей [FieldIndex](../com.aspose.words/fieldindex/) в документе. |
| [FieldInfo](../com.aspose.words/fieldinfo/) | Реализует поле INFO. |
| [FieldKeywords](../com.aspose.words/fieldkeywords/) | Реализует поле KEYWORDS. |
| [FieldLastSavedBy](../com.aspose.words/fieldlastsavedby/) | Реализует поле LASTSAVEDBY. |
| [FieldLink](../com.aspose.words/fieldlink/) | Реализует поле LINK. |
| [FieldListNum](../com.aspose.words/fieldlistnum/) | Реализует поле LISTNUM. |
| [FieldMacroButton](../com.aspose.words/fieldmacrobutton/) | Реализует поле MACROBUTTON. |
| [FieldMergeBarcode](../com.aspose.words/fieldmergebarcode/) | Реализует поле MERGEBARCODE. |
| [FieldMergeField](../com.aspose.words/fieldmergefield/) | Реализует поле MERGEFIELD. |
| [FieldMergeRec](../com.aspose.words/fieldmergerec/) | Реализует поле MERGEREC. |
| [FieldMergeSeq](../com.aspose.words/fieldmergeseq/) | Реализует поле MERGESEQ. |
| [FieldMergingArgs](../com.aspose.words/fieldmergingargs/) | Предоставляет данные для события **MergeField**. |
| [FieldMergingArgsBase](../com.aspose.words/fieldmergingargsbase/) | Базовый класс для [FieldMergingArgs](../com.aspose.words/fieldmergingargs/) и [ImageFieldMergingArgs](../com.aspose.words/imagefieldmergingargs/). |
| [FieldNext](../com.aspose.words/fieldnext/) | Реализует поле NEXT. |
| [FieldNextIf](../com.aspose.words/fieldnextif/) | Реализует поле NEXTIF. |
| [FieldNoteRef](../com.aspose.words/fieldnoteref/) | Реализует поле NOTEREF. |
| [FieldNumChars](../com.aspose.words/fieldnumchars/) | Реализует поле NUMCHARS. |
| [FieldNumPages](../com.aspose.words/fieldnumpages/) | Реализует поле NUMPAGES. |
| [FieldNumWords](../com.aspose.words/fieldnumwords/) | Реализует поле NUMWORDS. |
| [FieldOcx](../com.aspose.words/fieldocx/) | Реализует поле OCX. |
| [FieldOptions](../com.aspose.words/fieldoptions/) | Представляет параметры для управления обработкой полей в документе. |
| [FieldPage](../com.aspose.words/fieldpage/) | Реализует поле PAGE. |
| [FieldPageRef](../com.aspose.words/fieldpageref/) | Реализует поле PAGEREF. |
| [FieldPrint](../com.aspose.words/fieldprint/) | Реализует поле PRINT. |
| [FieldPrintDate](../com.aspose.words/fieldprintdate/) | Реализует поле PRINTDATE. |
| [FieldPrivate](../com.aspose.words/fieldprivate/) | Реализует поле PRIVATE. |
| [FieldQuote](../com.aspose.words/fieldquote/) | Реализует поле QUOTE. |
| [FieldRD](../com.aspose.words/fieldrd/) | Реализует поле RD. |
| [FieldRef](../com.aspose.words/fieldref/) | Реализует поле REF. |
| [FieldRevNum](../com.aspose.words/fieldrevnum/) | Реализует поле REVNUM. |
| [FieldSaveDate](../com.aspose.words/fieldsavedate/) | Реализует поле SAVEDATE. |
| [FieldSection](../com.aspose.words/fieldsection/) | Реализует поле SECTION. |
| [FieldSectionPages](../com.aspose.words/fieldsectionpages/) | Реализует поле SECTIONPAGES. |
| [FieldSeparator](../com.aspose.words/fieldseparator/) | Представляет разделитель полей Word, который отделяет код поля от результата поля. |
| [FieldSeq](../com.aspose.words/fieldseq/) | Реализует поле SEQ. |
| [FieldSet](../com.aspose.words/fieldset/) | Реализует поле SET. |
| [FieldShape](../com.aspose.words/fieldshape/) | Реализует поле SHAPE. |
| [FieldSkipIf](../com.aspose.words/fieldskipif/) | Реализует поле SKIPIF. |
| [FieldStart](../com.aspose.words/fieldstart/) | Представляет начало поля Word в документе. |
| [FieldStyleRef](../com.aspose.words/fieldstyleref/) | Реализует поле STYLEREF. |
| [FieldSubject](../com.aspose.words/fieldsubject/) | Реализует поле SUBJECT. |
| [FieldSymbol](../com.aspose.words/fieldsymbol/) | Реализует поле SYMBOL. |
| [FieldTA](../com.aspose.words/fieldta/) | Реализует поле TA. |
| [FieldTC](../com.aspose.words/fieldtc/) | Реализует поле TC. |
| [FieldTemplate](../com.aspose.words/fieldtemplate/) | Реализует поле TEMPLATE. |
| [FieldTime](../com.aspose.words/fieldtime/) | Реализует поле TIME. |
| [FieldTitle](../com.aspose.words/fieldtitle/) | Реализует поле TITLE. |
| [FieldToa](../com.aspose.words/fieldtoa/) | Реализует поле TOA. |
| [FieldToc](../com.aspose.words/fieldtoc/) | Реализует поле TOC. |
| [FieldType](../com.aspose.words/fieldtype/) | Указывает типы полей Microsoft Word. |
| [FieldUnknown](../com.aspose.words/fieldunknown/) | Реализует неизвестное или нераспознанное поле. |
| [FieldUpdateCultureSource](../com.aspose.words/fieldupdateculturesource/) | Указывает, какую культуру использовать при обновлении поля. |
| [FieldUpdatingProgressArgs](../com.aspose.words/fieldupdatingprogressargs/) | Предоставляет данные для события прогресса обновления поля. |
| [FieldUserAddress](../com.aspose.words/fielduseraddress/) | Реализует поле USERADDRESS. |
| [FieldUserInitials](../com.aspose.words/fielduserinitials/) | Реализует поле USERINITIALS. |
| [FieldUserName](../com.aspose.words/fieldusername/) | Реализует поле USERNAME. |
| [FieldXE](../com.aspose.words/fieldxe/) | Реализует поле XE. |
| [FileCorruptedException](../com.aspose.words/filecorruptedexception/) | Выбрасывается при загрузке документа, когда документ кажется повреждённым и его невозможно загрузить. |
| [FileFontSource](../com.aspose.words/filefontsource/) | Представляет единственный файл шрифта TrueType, хранящийся в файловой системе. |
| [FileFormatInfo](../com.aspose.words/fileformatinfo/) | Содержит данные, возвращаемые методами обнаружения формата документа [FileFormatUtil](../com.aspose.words/fileformatutil/). |
| [FileFormatUtil](../com.aspose.words/fileformatutil/) | Предоставляет вспомогательные методы для работы с форматами файлов, такие как определение формата файла или преобразование расширений файлов в/из перечислений форматов файлов. |
| [Fill](../com.aspose.words/fill/) | Представляет формат заполнения для объекта. |
| [FillType](../com.aspose.words/filltype/) | Указывает тип заполнения для заполняемого объекта. |
| [FindReplaceDirection](../com.aspose.words/findreplacedirection/) | Указывает направление для операций замены. |
| [FindReplaceOptions](../com.aspose.words/findreplaceoptions/) | Указывает параметры для операций поиска/замены. |
| [FipsUnapprovedOperationException](../com.aspose.words/fipsunapprovedoperationexception/) | Представляет исключение, которое выбрасывается при неправильной попытке использовать криптографию. |
| [FixedPageSaveOptions](../com.aspose.words/fixedpagesaveoptions/) | Содержит общие параметры, которые можно указать при сохранении документа в фиксированные форматы страниц (PDF, XPS, изображения и т.д.). |
| [FlipOrientation](../com.aspose.words/fliporientation/) | Возможные значения ориентации фигуры. |
| [FolderFontSource](../com.aspose.words/folderfontsource/) | Представляет папку, содержащую файлы шрифтов TrueType. |
| [Font](../com.aspose.words/font/) | Содержит атрибуты шрифта (название шрифта, размер шрифта, цвет и т.д.) для объекта. |
| [FontConfigSubstitutionRule](../com.aspose.words/fontconfigsubstitutionrule/) | Правило замены конфигурации шрифта. |
| [FontEmbeddingLicensingRights](../com.aspose.words/fontembeddinglicensingrights/) | Представляет права лицензии на встраивание шрифта. |
| [FontEmbeddingUsagePermissions](../com.aspose.words/fontembeddingusagepermissions/) | Представляет разрешения на использование встраивания шрифта. |
| [FontFallbackSettings](../com.aspose.words/fontfallbacksettings/) | Указывает настройки механизма резервного шрифта. |
| [FontFamily](../com.aspose.words/fontfamily/) | Представляет семейство шрифтов. |
| [FontFeature](../com.aspose.words/fontfeature/) | Функции предоставляют информацию о том, как глифы используются в шрифте для отображения сценария. |
| [FontInfo](../com.aspose.words/fontinfo/) | Указывает информацию о шрифте, используемом в документе. |
| [FontInfoCollection](../com.aspose.words/fontinfocollection/) | Представляет коллекцию шрифтов, используемых в документе. |
| [FontInfoSubstitutionRule](../com.aspose.words/fontinfosubstitutionrule/) | Правило замены информации о шрифте. |
| [FontNameSubstitutionRule](../com.aspose.words/fontnamesubstitutionrule/) | Правило замены шрифта для обработки названия шрифта. |
| [FontPitch](../com.aspose.words/fontpitch/) | Представляет шаг шрифта. |
| [FontSavingArgs](../com.aspose.words/fontsavingargs/) | Предоставляет данные для события [IFontSavingCallback.#fontSaving(com.aspose.words.FontSavingArgs)](../com.aspose.words/ifontsavingcallback/#fontSaving-com.aspose.words.FontSavingArgs). |
| [FontSettings](../com.aspose.words/fontsettings/) | Указывает настройки шрифта для документа. |
| [FontSourceBase](../com.aspose.words/fontsourcebase/) | Это абстрактный базовый класс для классов, позволяющих пользователю указывать различные источники шрифтов. |
| [FontSourceType](../com.aspose.words/fontsourcetype/) | Указывает тип источника шрифта. |
| [FontSubstitutionReason](../com.aspose.words/fontsubstitutionreason/) | Указывает причину замены шрифта. |
| [FontSubstitutionRule](../com.aspose.words/fontsubstitutionrule/) | Это абстрактный базовый класс для правила замены шрифта. |
| [FontSubstitutionSettings](../com.aspose.words/fontsubstitutionsettings/) | Указывает настройки механизма замены шрифта. |
| [FontSubstitutionWarningInfo](../com.aspose.words/fontsubstitutionwarninginfo/) | Содержит информацию о предупреждении о замене шрифта, выданном Aspose.Words во время загрузки или сохранения документа. |
| [Footnote](../com.aspose.words/footnote/) | Представляет контейнер для текста сноски или концевой сноски. |
| [FootnoteNumberingRule](../com.aspose.words/footnotenumberingrule/) | Определяет, когда автоматическая нумерация сносок или концевых сносок перезапускается. |
| [FootnoteOptions](../com.aspose.words/footnoteoptions/) | Представляет параметры нумерации сносок для документа или раздела. |
| [FootnotePosition](../com.aspose.words/footnoteposition/) | Определяет положение сноски. |
| [FootnoteSeparator](../com.aspose.words/footnoteseparator/) |  |
| [FootnoteSeparatorCollection](../com.aspose.words/footnoteseparatorcollection/) | Обеспечивает типизированный доступ к узлам **T:Aspose.Words.Notes.FootnoteSeparator** документа. |
| [FootnoteSeparatorType](../com.aspose.words/footnoteseparatortype/) | Указывает тип разделителя сноски/концевой сноски. |
| [FootnoteType](../com.aspose.words/footnotetype/) | Указывает, является ли это сноской или концевой сноской. |
| [FormField](../com.aspose.words/formfield/) | Представляет отдельное поле формы. |
| [FormFieldCollection](../com.aspose.words/formfieldcollection/) | Коллекция объектов [FormField](../com.aspose.words/formfield/), представляющих все поля формы в диапазоне. |
| [Forms2OleControl](../com.aspose.words/forms2olecontrol/) | Представляет OLE‑элемент Microsoft Forms 2.0. |
| [Forms2OleControlCollection](../com.aspose.words/forms2olecontrolcollection/) | Представляет коллекцию объектов [Forms2OleControl](../com.aspose.words/forms2olecontrol/). |
| [Forms2OleControlType](../com.aspose.words/forms2olecontroltype/) | Перечисляет типы элементов управления Forms 2.0. |
| [FrameFormat](../com.aspose.words/frameformat/) | Представляет форматирование, связанное с рамкой, для абзаца. |
| [Frameset](../com.aspose.words/frameset/) | Представляет страницу с рамками или отдельную рамку на странице с рамками. |
| [FramesetCollection](../com.aspose.words/framesetcollection/) | Представляет коллекцию экземпляров класса [Frameset](../com.aspose.words/frameset/). |
| [GeneralFormat](../com.aspose.words/generalformat/) | Указывает общий формат, применяемый к числовому, текстовому или любому результату поля. |
| [GeneralFormatCollection](../com.aspose.words/generalformatcollection/) | Представляет типизированную коллекцию общих форматов. |
| [GlossaryDocument](../com.aspose.words/glossarydocument/) | Представляет корневой элемент глоссария внутри документа Word. |
| [GlowFormat](../com.aspose.words/glowformat/) | Представляет свечение объекта. |
| [Glyph](../com.aspose.words/glyph/) | Представляет глиф |
| [GlyphFlags](../com.aspose.words/glyphflags/) |  |
| [GoogleAiModel](../com.aspose.words/googleaimodel/) | Класс, представляющий интеграцию моделей Google AI (Gemini) в Aspose.Words. |
| [GradientStop](../com.aspose.words/gradientstop/) | Представляет одну точку градиента. |
| [GradientStopCollection](../com.aspose.words/gradientstopcollection/) | Содержит коллекцию объектов [GradientStop](../com.aspose.words/gradientstop/). |
| [GradientStyle](../com.aspose.words/gradientstyle/) | Указывает стиль градиентной заливки. |
| [GradientVariant](../com.aspose.words/gradientvariant/) | Указывает вариант градиентной заливки. |
| [Granularity](../com.aspose.words/granularity/) | Указывает степень детализации изменений для отслеживания при сравнении двух документов. |
| [GraphicsQualityOptions](../com.aspose.words/graphicsqualityoptions/) | Позволяет указать дополнительные **java.awt.RenderingHints**. |
| [GroupShape](../com.aspose.words/groupshape/) | Представляет группу фигур в документе. |
| [HeaderFooter](../com.aspose.words/headerfooter/) | Представляет контейнер для текста верхнего или нижнего колонтитула раздела. |
| [HeaderFooterBookmarksExportMode](../com.aspose.words/headerfooterbookmarksexportmode/) | Указывает, как экспортируются закладки в верхних/нижних колонтитулах. |
| [HeaderFooterCollection](../com.aspose.words/headerfootercollection/) | Обеспечивает типизированный доступ к узлам [HeaderFooter](../com.aspose.words/headerfooter/) и [Section](../com.aspose.words/section/). |
| [HeaderFooterType](../com.aspose.words/headerfootertype/) | Определяет тип верхнего или нижнего колонтитула, найденного в файле Word. |
| [HeightRule](../com.aspose.words/heightrule/) | Указывает правило определения высоты объекта. |
| [HorizontalAlignment](../com.aspose.words/horizontalalignment/) | Указывает горизонтальное выравнивание плавающей фигуры, текстовой рамки или плавающей таблицы. |
| [HorizontalRuleAlignment](../com.aspose.words/horizontalrulealignment/) | Представляет выравнивание для указанного горизонтального правила. |
| [HorizontalRuleFormat](../com.aspose.words/horizontalruleformat/) | Представляет форматирование горизонтального правила. |
| [HtmlControlType](../com.aspose.words/htmlcontroltype/) | Тип узлов документа, представляющих элементы  и  , импортированные из HTML. |
| [HtmlElementSizeOutputMode](../com.aspose.words/htmlelementsizeoutputmode/) | Указывает, как Aspose.Words экспортирует ширину и высоту элементов в HTML, MHTML и EPUB. |
| [HtmlFixedPageHorizontalAlignment](../com.aspose.words/htmlfixedpagehorizontalalignment/) | Указывает горизонтальное выравнивание страниц в выводимом HTML‑документе. |
| [HtmlFixedSaveOptions](../com.aspose.words/htmlfixedsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#HTML\_FIXED](../com.aspose.words/saveformat/\#HTML-FIXED). |
| [HtmlInsertOptions](../com.aspose.words/htmlinsertoptions/) | Указывает параметры для метода **M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)**. |
| [HtmlLoadOptions](../com.aspose.words/htmlloadoptions/) | Позволяет указать дополнительные параметры при загрузке HTML‑документа в объект [Document](../com.aspose.words/document/). |
| [HtmlMetafileFormat](../com.aspose.words/htmlmetafileformat/) | Указывает формат, в котором метафайлы сохраняются в HTML‑документы. |
| [HtmlOfficeMathOutputMode](../com.aspose.words/htmlofficemathoutputmode/) | Указывает, как Aspose.Words экспортирует OfficeMath в HTML, MHTML и EPUB. |
| [HtmlSaveOptions](../com.aspose.words/htmlsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML), [SaveFormat.\#MHTML](../com.aspose.words/saveformat/\#MHTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB), [SaveFormat.\#AZW\_3](../com.aspose.words/saveformat/\#AZW-3) или [SaveFormat.\#MOBI](../com.aspose.words/saveformat/\#MOBI). |
| [HtmlVersion](../com.aspose.words/htmlversion/) | Указывает, какая версия HTML используется при сохранении документа в форматы [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML) и [SaveFormat.\#MHTML](../com.aspose.words/saveformat/\#MHTML). |
| [Hyphenation](../com.aspose.words/hyphenation/) | Предоставляет методы для работы со словарями переносов. |
| [HyphenationOptions](../com.aspose.words/hyphenationoptions/) | Позволяет настроить параметры переносов в документе. |
| [ImageBinarizationMethod](../com.aspose.words/imagebinarizationmethod/) | Указывает метод, используемый для бинаризации изображения. |
| [ImageColorMode](../com.aspose.words/imagecolormode/) | Указывает цветовой режим для генерируемых изображений страниц документа. |
| [ImageData](../com.aspose.words/imagedata/) | Определяет изображение для фигуры. |
| [ImageFieldMergingArgs](../com.aspose.words/imagefieldmergingargs/) | Предоставляет данные для события [IFieldMergingCallback.\#imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../com.aspose.words/ifieldmergingcallback/\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs). |
| [ImagePixelFormat](../com.aspose.words/imagepixelformat/) | Указывает пиксельный формат для генерируемых изображений страниц документа. |
| [ImageSaveOptions](../com.aspose.words/imagesaveoptions/) | Позволяет указывать дополнительные параметры при рендеринге страниц документа или фигур в изображения. |
| [ImageSavingArgs](../com.aspose.words/imagesavingargs/) | Предоставляет данные для события [IImageSavingCallback.#imageSaving(com.aspose.words.ImageSavingArgs)](../com.aspose.words/iimagesavingcallback/#imageSaving-com.aspose.words.ImageSavingArgs). |
| [ImageSize](../com.aspose.words/imagesize/) | Содержит информацию о размере изображения и разрешении. |
| [ImageType](../com.aspose.words/imagetype/) | Указывает тип (формат) изображения в документе Microsoft Word. |
| [ImageWatermarkOptions](../com.aspose.words/imagewatermarkoptions/) | Содержит параметры, которые можно указать при добавлении водяного знака с изображением. |
| [ImlRenderingMode](../com.aspose.words/imlrenderingmode/) | Указывает, как объекты чернил (InkML) рендерятся в фиксированные форматы страниц. |
| [ImportFormatMode](../com.aspose.words/importformatmode/) | Указывает, как форматирование объединяется при импорте содержимого из другого документа. |
| [ImportFormatOptions](../com.aspose.words/importformatoptions/) | Позволяет указывать различные параметры импорта для форматирования вывода. |
| [IncorrectPasswordException](../com.aspose.words/incorrectpasswordexception/) | Выбрасывается, если документ зашифрован паролем, а указанный при открытии документа пароль неверен или отсутствует. |
| [Inline](../com.aspose.words/inline/) | Базовый класс для узлов уровня inline, которые могут иметь связанную символьную форматировку, но не могут иметь собственных дочерних узлов. |
| [InlineStory](../com.aspose.words/inlinestory/) | Базовый класс для узлов уровня inline, которые могут содержать абзацы и таблицы. |
| [InternableComplexAttr](../com.aspose.words/internablecomplexattr/) | Базовый класс для интернируемого сложного атрибута. |
| [JoinRunsOptions](../com.aspose.words/joinrunsoptions/) | Предоставляет флаги конфигурации для операции объединения пробегов. |
| [JoinStyle](../com.aspose.words/joinstyle/) | Стиль соединения линий. |
| [JsonDataLoadOptions](../com.aspose.words/jsondataloadoptions/) | Представляет параметры для разбора JSON-данных. |
| [JsonDataSource](../com.aspose.words/jsondatasource/) | Предоставляет доступ к данным JSON-файла или потока, которые будут использоваться в отчете. |
| [JsonSimpleValueParseMode](../com.aspose.words/jsonsimplevalueparsemode/) | Указывает режим разбора простых значений JSON (null, boolean, number, integer и string) при загрузке JSON. |
| [JustificationMode](../com.aspose.words/justificationmode/) | Указывает настройку межсимвольного интервала для документа. |
| [KnownTypeSet](../com.aspose.words/knowntypeset/) | Представляет неупорядоченный набор (т.е. |
| [Language](../com.aspose.words/language/) | Указывает язык, на который будет переведен текст с использованием ИИ. |
| [LanguagePreferences](../com.aspose.words/languagepreferences/) | Позволяет настроить языковые предпочтения. |
| [LayoutCollector](../com.aspose.words/layoutcollector/) | Этот класс позволяет вычислять номера страниц узлов документа. |
| [LayoutEntityType](../com.aspose.words/layoutentitytype/) | Типы сущностей компоновки. |
| [LayoutEnumerator](../com.aspose.words/layoutenumerator/) | Перечисляет сущности компоновки страниц документа. |
| [LayoutFlow](../com.aspose.words/layoutflow/) | Определяет поток компоновки текста в текстовом поле. |
| [LayoutOptions](../com.aspose.words/layoutoptions/) | Содержит параметры, позволяющие управлять процессом компоновки документа. |
| [LegendPosition](../com.aspose.words/legendposition/) | Указывает возможные позиции для легенды диаграммы. |
| [License](../com.aspose.words/license/) | Предоставляет методы для лицензирования компонента. |
| [LineNumberRestartMode](../com.aspose.words/linenumberrestartmode/) | Определяет, когда автоматическая нумерация строк перезапускается. |
| [LineSpacingRule](../com.aspose.words/linespacingrule/) | Указывает значения межстрочного интервала для абзаца. |
| [LineStyle](../com.aspose.words/linestyle/) | Указывает стиль линии [Border](../com.aspose.words/border/). |
| [List](../com.aspose.words/list/) | Представляет форматирование списка. |
| [ListCollection](../com.aspose.words/listcollection/) | Хранит и управляет форматированием маркированных и нумерованных списков, используемых в документе. |
| [ListFormat](../com.aspose.words/listformat/) | Позволяет контролировать, какое форматирование списка применяется к абзацу. |
| [ListLabel](../com.aspose.words/listlabel/) | Определяет свойства, специфичные для метки списка. |
| [ListLevel](../com.aspose.words/listlevel/) | Определяет форматирование уровня списка. |
| [ListLevelAlignment](../com.aspose.words/listlevelalignment/) | Указывает выравнивание номера списка или маркера. |
| [ListLevelCollection](../com.aspose.words/listlevelcollection/) | Коллекция форматирования списка для каждого уровня в списке. |
| [ListTemplate](../com.aspose.words/listtemplate/) | Указывает один из предопределённых форматов списков, доступных в Microsoft Word. |
| [ListTrailingCharacter](../com.aspose.words/listtrailingcharacter/) | Указывает символ, разделяющий метку списка и текст абзаца. |
| [LoadFormat](../com.aspose.words/loadformat/) | Указывает формат документа, который будет загружен. |
| [LoadOptions](../com.aspose.words/loadoptions/) | Позволяет указать дополнительные параметры (например, пароль или базовый URI) при загрузке документа в объект [Document](../com.aspose.words/document/). |
| [MailMerge](../com.aspose.words/mailmerge/) | Представляет функциональность слияния почты. |
| [MailMergeCheckErrors](../com.aspose.words/mailmergecheckerrors/) | Указывает, как Microsoft Word будет сообщать об ошибках, обнаруженных во время слияния почты. |
| [MailMergeCleanupOptions](../com.aspose.words/mailmergecleanupoptions/) | Указывает параметры, определяющие, какие элементы удаляются во время слияния почты. |
| [MailMergeDataSource](../com.aspose.words/mailmergedatasource/) | Источник данных слияния почты, используемый в [MailMergerContext](../com.aspose.words/mailmergercontext/). |
| [MailMergeDataType](../com.aspose.words/mailmergedatatype/) | Указывает тип внешнего источника данных слияния почты. |
| [MailMergeDestination](../com.aspose.words/mailmergedestination/) | Указывает возможные результаты, которые могут быть сгенерированы при выполнении слияния почты в документе. |
| [MailMergeMainDocumentType](../com.aspose.words/mailmergemaindocumenttype/) | Указывает возможные типы исходного документа слияния почты. |
| [MailMergeOptions](../com.aspose.words/mailmergeoptions/) | Представляет параметры для функциональности слияния почты. |
| [MailMergeRegionInfo](../com.aspose.words/mailmergeregioninfo/) | Содержит информацию о регионе слияния почты. |
| [MailMergeSettings](../com.aspose.words/mailmergesettings/) | Указывает всю информацию о слиянии почты для документа. |
| [MailMerger](../com.aspose.words/mailmerger/) | Предоставляет методы, предназначенные для заполнения шаблона данными с использованием простого слияния почты и операций слияния почты с регионами. |
| [MailMergerContext](../com.aspose.words/mailmergercontext/) | Контекст слияния почты. |
| [MappedDataFieldCollection](../com.aspose.words/mappeddatafieldcollection/) | Позволяет автоматически сопоставлять имена полей в вашем источнике данных с именами полей слияния почты в документе. |
| [Margins](../com.aspose.words/margins/) | Указывает предустановленные поля. |
| [MarkdownEmptyParagraphExportMode](../com.aspose.words/markdownemptyparagraphexportmode/) | Указывает, как Aspose.Words экспортирует пустые абзацы в Markdown. |
| [MarkdownExportAsHtml](../com.aspose.words/markdownexportashtml/) | Позволяет указать элементы, которые будут экспортированы в Markdown как необработанный HTML. |
| [MarkdownLinkExportMode](../com.aspose.words/markdownlinkexportmode/) | Указывает, как ссылки экспортируются в Markdown. |
| [MarkdownListExportMode](../com.aspose.words/markdownlistexportmode/) | Указывает, как списки экспортируются в Markdown. |
| [MarkdownLoadOptions](../com.aspose.words/markdownloadoptions/) | Позволяет указать дополнительные параметры при загрузке документа [LoadFormat.\#MARKDOWN](../com.aspose.words/loadformat/\#MARKDOWN) в объект [Document](../com.aspose.words/document/). |
| [MarkdownOfficeMathExportMode](../com.aspose.words/markdownofficemathexportmode/) | Указывает, как Aspose.Words экспортирует OfficeMath в Markdown. |
| [MarkdownSaveOptions](../com.aspose.words/markdownsaveoptions/) | Класс для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#MARKDOWN](../com.aspose.words/saveformat/\#MARKDOWN). |
| [MarkerSymbol](../com.aspose.words/markersymbol/) | Указывает стиль символа маркера. |
| [MarkupLevel](../com.aspose.words/markuplevel/) | Указывает уровень в дереве документа, где может появиться конкретный [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/). |
| [MathObjectType](../com.aspose.words/mathobjecttype/) | Указывает тип объекта Office Math. |
| [MeasurementUnits](../com.aspose.words/measurementunits/) | Указывает единицу измерения. |
| [MemoryFontSource](../com.aspose.words/memoryfontsource/) | Представляет отдельный файл шрифта TrueType, хранящийся в памяти. |
| [MergeFieldImageDimension](../com.aspose.words/mergefieldimagedimension/) | Представляет размер изображения (т.е. |
| [MergeFieldImageDimensionUnit](../com.aspose.words/mergefieldimagedimensionunit/) | Указывает единицу измерения размера изображения (т.е. |
| [MergeFormatMode](../com.aspose.words/mergeformatmode/) | Указывает, как форматирование объединяется при комбинировании нескольких документов. |
| [Merger](../com.aspose.words/merger/) | Представляет набор методов, предназначенных для объединения различных типов документов в один итоговый документ. |
| [MergerContext](../com.aspose.words/mergercontext/) | Контекст объединения документов. |
| [MetafileRenderingMode](../com.aspose.words/metafilerenderingmode/) | Указывает, как Aspose.Words должен отображать метафайлы WMF и EMF. |
| [MetafileRenderingOptions](../com.aspose.words/metafilerenderingoptions/) | Позволяет указать дополнительные параметры отображения метафайлов. |
| [Metered](../com.aspose.words/metered/) | Предоставляет методы для установки измеряемого ключа. |
| [MorphDataControl](../com.aspose.words/morphdatacontrol/) | Структура MorphDataControl представляет собой совокупность шести элементов управления: CheckBox, ComboBox, ListBox, OptionButton, TextBox и ToggleButton. |
| [MsWordVersion](../com.aspose.words/mswordversion/) | Позволяет Aspose.Wods имитировать поведение приложения, специфичное для версии MS Word. |
| [MultiPageLayout](../com.aspose.words/multipagelayout/) | Определяет макет для рендеринга нескольких страниц в один вывод. |
| [MultiplePagesType](../com.aspose.words/multiplepagestype/) | Указывает, как документ печатается. |
| [MustacheTag](../com.aspose.words/mustachetag/) | Представляет тег "mustache". |
| [NativeLibSettings](../com.aspose.words/nativelibsettings/) | Этот класс помогает установить различные параметры, такие как временная папка для нативных библиотек Aspose.Words и то, должны ли нативные библиотеки загружаться и использоваться. |
| [Node](../com.aspose.words/node/) | Базовый класс для всех узлов документа Word. |
| [NodeChangingAction](../com.aspose.words/nodechangingaction/) | Указывает тип изменения узла. |
| [NodeChangingArgs](../com.aspose.words/nodechangingargs/) | Предоставляет данные для методов интерфейса [INodeChangingCallback](../com.aspose.words/inodechangingcallback/). |
| [NodeCollection](../com.aspose.words/nodecollection/) | Представляет коллекцию узлов определённого типа. |
| [NodeImporter](../com.aspose.words/nodeimporter/) | Позволяет эффективно выполнять повторный импорт узлов из одного документа в другой. |
| [NodeList](../com.aspose.words/nodelist/) | Представляет коллекцию узлов, соответствующих XPath‑запросу, выполненному с помощью метода [CompositeNode.\#selectNodes(java.lang.String)](../com.aspose.words/compositenode/\#selectNodes-java.lang.String). |
| [NodeRendererBase](../com.aspose.words/noderendererbase/) | Базовый класс для [ShapeRenderer](../com.aspose.words/shaperenderer/) и [OfficeMathRenderer](../com.aspose.words/officemathrenderer/). |
| [NodeType](../com.aspose.words/nodetype/) | Указывает тип узла документа Word. |
| [NumSpacing](../com.aspose.words/numspacing/) | Указывает возможные значения, в которых может отображаться интервал между цифрами. |
| [NumberStyle](../com.aspose.words/numberstyle/) | Указывает стиль нумерации для списка, сносок и концевых сносок, номеров страниц. |
| [NumeralFormat](../com.aspose.words/numeralformat/) | Указывает набор символов, используемый для представления чисел при рендеринге в фиксированные форматы страниц. |
| [Odso](../com.aspose.words/odso/) | Указывает настройки Office Data Source Object (ODSO) для источника данных слияния писем. |
| [OdsoDataSourceType](../com.aspose.words/odsodatasourcetype/) | Указывает тип внешнего источника данных, к которому следует подключиться в рамках информации о соединении ODSO. |
| [OdsoFieldMapData](../com.aspose.words/odsofieldmapdata/) | Указывает, как столбец во внешнем источнике данных будет сопоставлен с предопределёнными полями слияния в документе. |
| [OdsoFieldMapDataCollection](../com.aspose.words/odsofieldmapdatacollection/) | Типизированная коллекция объектов [OdsoFieldMapData](../com.aspose.words/odsofieldmapdata/). |
| [OdsoFieldMappingType](../com.aspose.words/odsofieldmappingtype/) | Указывает возможные типы, используемые для обозначения того, сопоставлено ли данное поле слияния с колонкой во внешнем источнике данных. |
| [OdsoRecipientData](../com.aspose.words/odsorecipientdata/) | Представляет информацию о отдельной записи во внешнем источнике данных, которая должна быть исключена из слияния писем. |
| [OdsoRecipientDataCollection](../com.aspose.words/odsorecipientdatacollection/) | Типизированная коллекция [OdsoRecipientData](../com.aspose.words/odsorecipientdata/) |
| [OdtSaveMeasureUnit](../com.aspose.words/odtsavemeasureunit/) | Указанные единицы измерения, применяемые к измеримому содержимому документа, такому как формы, ширины и другое при сохранении. |
| [OdtSaveOptions](../com.aspose.words/odtsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.#ODT](../com.aspose.words/saveformat/#ODT) или [SaveFormat.#OTT](../com.aspose.words/saveformat/#OTT). |
| [OfficeMath](../com.aspose.words/officemath/) | Представляет объект Office Math, такой как функция, уравнение, матрица или аналогичный. |
| [OfficeMathDisplayType](../com.aspose.words/officemathdisplaytype/) | Указывает тип формата отображения уравнения. |
| [OfficeMathJustification](../com.aspose.words/officemathjustification/) | Указывает выравнивание уравнения. |
| [OfficeMathRenderer](../com.aspose.words/officemathrenderer/) | Предоставляет методы для рендеринга отдельного [OfficeMath](../com.aspose.words/officemath/) в растровое или векторное изображение или в объект Graphics. |
| [OleControl](../com.aspose.words/olecontrol/) | Представляет элемент управления OLE ActiveX. |
| [OleFormat](../com.aspose.words/oleformat/) | Обеспечивает доступ к данным OLE‑объекта или элемента управления ActiveX. |
| [OlePackage](../com.aspose.words/olepackage/) | Позволяет получать доступ к свойствам OLE Package. |
| [OoxmlCompliance](../com.aspose.words/ooxmlcompliance/) | Позволяет указать, какая спецификация OOXML будет использоваться при сохранении в формате DOCX. |
| [OoxmlSaveOptions](../com.aspose.words/ooxmlsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.#DOCX](../com.aspose.words/saveformat/#DOCX), [SaveFormat.#DOCM](../com.aspose.words/saveformat/#DOCM), [SaveFormat.#DOTX](../com.aspose.words/saveformat/#DOTX), [SaveFormat.#DOTM](../com.aspose.words/saveformat/#DOTM) или [SaveFormat.#FLAT_OPC](../com.aspose.words/saveformat/#FLAT-OPC). |
| [OpenAiModel](../com.aspose.words/openaimodel/) | Класс, представляющий интеграцию моделей OpenAi в Aspose.Words. |
| [OptionButtonControl](../com.aspose.words/optionbuttoncontrol/) | Элемент управления OptionButton позволяет сделать единственный выбор из ограниченного набора взаимно исключающих вариантов. |
| [Orientation](../com.aspose.words/orientation/) | Указывает ориентацию страницы. |
| [OutlineLevel](../com.aspose.words/outlinelevel/) | Указывает уровень структуры абзаца в документе. |
| [OutlineOptions](../com.aspose.words/outlineoptions/) | Позволяет указать параметры структуры. |
| [PageBorderAppliesTo](../com.aspose.words/pageborderappliesto/) | Указывает, на каких страницах печатается граница страницы. |
| [PageBorderDistanceFrom](../com.aspose.words/pageborderdistancefrom/) | Указывает позиционирование границы страницы относительно полей страницы. |
| [PageExtractOptions](../com.aspose.words/pageextractoptions/) | Позволяет указать параметры извлечения страниц документа. |
| [PageInfo](../com.aspose.words/pageinfo/) | Представляет информацию о конкретной странице документа. |
| [PageLayoutCallbackArgs](../com.aspose.words/pagelayoutcallbackargs/) | Аргумент, передаваемый в [IPageLayoutCallback.#notify(com.aspose.words.PageLayoutCallbackArgs)](../com.aspose.words/ipagelayoutcallback/#notify-com.aspose.words.PageLayoutCallbackArgs) |
| [PageLayoutEvent](../com.aspose.words/pagelayoutevent/) | Код события, вызываемого во время построения и рендеринга модели разметки страниц. |
| [PageRange](../com.aspose.words/pagerange/) | Представляет непрерывный диапазон страниц. |
| [PageSavingArgs](../com.aspose.words/pagesavingargs/) | Предоставляет данные для события [IPageSavingCallback.#pageSaving(com.aspose.words.PageSavingArgs)](../com.aspose.words/ipagesavingcallback/#pageSaving-com.aspose.words.PageSavingArgs). |
| [PageSet](../com.aspose.words/pageset/) | Описывает случайный набор страниц. |
| [PageSetup](../com.aspose.words/pagesetup/) | Представляет свойства настройки страницы раздела. |
| [PageVerticalAlignment](../com.aspose.words/pageverticalalignment/) | Указывает вертикальное выравнивание текста на каждой странице. |
| [PaperSize](../com.aspose.words/papersize/) | Указывает размер бумаги. |
| [Paragraph](../com.aspose.words/paragraph/) | Представляет абзац текста. |
| [ParagraphAlignment](../com.aspose.words/paragraphalignment/) | Указывает выравнивание текста в абзаце. |
| [ParagraphCollection](../com.aspose.words/paragraphcollection/) | Обеспечивает типизированный доступ к коллекции узлов [Paragraph](../com.aspose.words/paragraph/). |
| [ParagraphFormat](../com.aspose.words/paragraphformat/) | Представляет всё форматирование абзаца. |
| [PatternType](../com.aspose.words/patterntype/) | Указывает шаблон заливки, используемый для заполнения фигуры. |
| [PclSaveOptions](../com.aspose.words/pclsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#PCL](../com.aspose.words/saveformat/\#PCL). |
| [PdfAttachmentsEmbeddingMode](../com.aspose.words/pdfattachmentsembeddingmode/) | Указывает, как вложения встраиваются в PDF‑документ. |
| [PdfCompliance](../com.aspose.words/pdfcompliance/) | Указывает уровень соответствия стандартам PDF. |
| [PdfCustomPropertiesExport](../com.aspose.words/pdfcustompropertiesexport/) | Указывает способ, которым [Document.\#getCustomDocumentProperties()](../com.aspose.words/document/\#getCustomDocumentProperties) экспортируются в PDF‑файл. |
| [PdfDigitalSignatureDetails](../com.aspose.words/pdfdigitalsignaturedetails/) | Содержит детали подписи PDF‑документа цифровой подписью. |
| [PdfDigitalSignatureHashAlgorithm](../com.aspose.words/pdfdigitalsignaturehashalgorithm/) | Указывает алгоритм цифрового хеша, используемый цифровой подписью. |
| [PdfDigitalSignatureTimestampSettings](../com.aspose.words/pdfdigitalsignaturetimestampsettings/) | Содержит настройки временной метки цифровой подписи. |
| [PdfEncryptionDetails](../com.aspose.words/pdfencryptiondetails/) | Содержит детали шифрования и прав доступа к PDF‑документу. |
| [PdfFontEmbeddingMode](../com.aspose.words/pdffontembeddingmode/) | Указывает, как Aspose.Words должен встраивать шрифты. |
| [PdfImageColorSpaceExportMode](../com.aspose.words/pdfimagecolorspaceexportmode/) | Указывает, как будет выбран цветовое пространство для изображений в PDF‑документе. |
| [PdfImageCompression](../com.aspose.words/pdfimagecompression/) | Указывает тип сжатия, применяемый к изображениям в PDF‑файле. |
| [PdfLoadOptions](../com.aspose.words/pdfloadoptions/) | Позволяет указать дополнительные параметры при загрузке Pdf документа в объект [Document](../com.aspose.words/document/). |
| [PdfPageLayout](../com.aspose.words/pdfpagelayout/) | Указывает макет страницы, используемый при открытии документа в PDF‑просмотрщике. |
| [PdfPageMode](../com.aspose.words/pdfpagemode/) | Указывает, как PDF‑документ должен отображаться при открытии в PDF‑просмотрщике. |
| [PdfPermissions](../com.aspose.words/pdfpermissions/) | Указывает операции, разрешённые пользователю в зашифрованном PDF‑документе. |
| [PdfSaveOptions](../com.aspose.words/pdfsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#PDF](../com.aspose.words/saveformat/\#PDF). |
| [PdfTextCompression](../com.aspose.words/pdftextcompression/) | Указывает тип сжатия, применяемый ко всему содержимому PDF‑файла, кроме изображений. |
| [PdfZoomBehavior](../com.aspose.words/pdfzoombehavior/) | Указывает тип масштабирования, применяемого к PDF‑документу при его открытии в PDF‑просмотрщике. |
| [Person](../com.aspose.words/person/) | Представляет отдельного (человека) участника библиографического источника. |
| [PersonCollection](../com.aspose.words/personcollection/) | Представляет список лиц, являющихся участниками библиографического источника. |
| [PhoneticGuide](../com.aspose.words/phoneticguide/) | Представляет фонетический справочник. |
| [PhysicalFontInfo](../com.aspose.words/physicalfontinfo/) | Указывает информацию о физическом шрифте, доступном движку шрифтов Aspose.Words. |
| [PlainTextDocument](../com.aspose.words/plaintextdocument/) | Позволяет извлекать текстовое представление содержимого документа. |
| [PreferredWidth](../com.aspose.words/preferredwidth/) | Представляет значение и его единицу измерения, используемые для указания предпочтительной ширины таблицы или ячейки. |
| [PreferredWidthType](../com.aspose.words/preferredwidthtype/) | Указывает единицу измерения предпочтительной ширины таблицы или ячейки. |
| [PresetTexture](../com.aspose.words/presettexture/) | Указывает текстуру, используемую для заполнения фигуры. |
| [Processor](../com.aspose.words/processor/) | Класс процессора для выполнения различных действий по обработке документов. |
| [ProcessorContext](../com.aspose.words/processorcontext/) | Базовый класс для контекстов процессора. |
| [PropertyType](../com.aspose.words/propertytype/) | Указывает тип данных свойства документа. |
| [ProtectionType](../com.aspose.words/protectiontype/) | Тип защиты документа. |
| [PsSaveOptions](../com.aspose.words/pssaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.#PS](../com.aspose.words/saveformat/#PS). |
| [Range](../com.aspose.words/range/) | Представляет непрерывную область в документе. |
| [ReadabilityStatistics](../com.aspose.words/readabilitystatistics/) | Предоставляет информацию о показателе читаемости документа. |
| [ReflectionFormat](../com.aspose.words/reflectionformat/) | Представляет форматирование отражения для объекта. |
| [RelativeHorizontalPosition](../com.aspose.words/relativehorizontalposition/) | Указывает, относительно чего определяется горизонтальное положение фигуры или текстового кадра. |
| [RelativeHorizontalSize](../com.aspose.words/relativehorizontalsize/) | Указывает, относительно чего рассчитывается горизонтальная ширина фигуры или текстового кадра. |
| [RelativeVerticalPosition](../com.aspose.words/relativeverticalposition/) | Указывает, относительно чего определяется вертикальное положение фигуры или текстового кадра. |
| [RelativeVerticalSize](../com.aspose.words/relativeverticalsize/) | Указывает, относительно чего рассчитывается вертикальная высота фигуры или текстового кадра. |
| [ReplaceAction](../com.aspose.words/replaceaction/) | Позволяет пользователю указать, что происходит с текущим совпадением во время операции замены. |
| [ReplacementFormat](../com.aspose.words/replacementformat/) | Указывает формат замены. |
| [Replacer](../com.aspose.words/replacer/) | Предоставляет методы, предназначенные для поиска и замены текста в документе. |
| [ReplacerContext](../com.aspose.words/replacercontext/) | Контекст операции поиска/замены. |
| [ReplacingArgs](../com.aspose.words/replacingargs/) | Предоставляет данные для пользовательской операции замены. |
| [ReportBuildOptions](../com.aspose.words/reportbuildoptions/) | Указывает параметры, контролирующие поведение [ReportingEngine](../com.aspose.words/reportingengine/) при построении отчёта. |
| [ReportBuilder](../com.aspose.words/reportbuilder/) | Предоставляет методы, предназначенные для заполнения шаблона данными с использованием LINQ Reporting Engine. |
| [ReportBuilderContext](../com.aspose.words/reportbuildercontext/) | Контекст LINQ Reporting Engine. |
| [ReportBuilderOptions](../com.aspose.words/reportbuilderoptions/) | Представляет параметры для функциональности LINQ Reporting Engine. |
| [ReportingEngine](../com.aspose.words/reportingengine/) | Предоставляет процедуры для заполнения шаблонных документов данными и набор настроек для управления этими процедурами. |
| [ResourceLoadingAction](../com.aspose.words/resourceloadingaction/) | Указывает режим загрузки ресурсов. |
| [ResourceLoadingArgs](../com.aspose.words/resourceloadingargs/) | Предоставляет данные для метода [IResourceLoadingCallback.\#resourceLoading(com.aspose.words.ResourceLoadingArgs)](../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs). |
| [ResourceSavingArgs](../com.aspose.words/resourcesavingargs/) | Предоставляет данные для события [IResourceSavingCallback.\#resourceSaving(com.aspose.words.ResourceSavingArgs)](../com.aspose.words/iresourcesavingcallback/\#resourceSaving-com.aspose.words.ResourceSavingArgs). |
| [ResourceType](../com.aspose.words/resourcetype/) | Тип загруженного ресурса. |
| [Revision](../com.aspose.words/revision/) | Представляет ревизию (отслеживаемое изменение) в узле документа или стиле. |
| [RevisionCollection](../com.aspose.words/revisioncollection/) | Коллекция объектов [Revision](../com.aspose.words/revision/), представляющих ревизии в документе. |
| [RevisionColor](../com.aspose.words/revisioncolor/) | Позволяет указать цвет ревизий документа. |
| [RevisionGroup](../com.aspose.words/revisiongroup/) | Представляет группу последовательных объектов [Revision](../com.aspose.words/revision/). |
| [RevisionGroupCollection](../com.aspose.words/revisiongroupcollection/) | Коллекция объектов [RevisionGroup](../com.aspose.words/revisiongroup/), представляющих группы ревизий в документе. |
| [RevisionOptions](../com.aspose.words/revisionoptions/) | Позволяет управлять тем, как ревизии документа обрабатываются во время процесса разметки. |
| [RevisionTextEffect](../com.aspose.words/revisiontexteffect/) | Позволяет указать эффект декорирования для ревизий текста документа. |
| [RevisionType](../com.aspose.words/revisiontype/) | Указывает тип изменения, отслеживаемого в [Revision](../com.aspose.words/revision/). |
| [RevisionsView](../com.aspose.words/revisionsview/) | Позволяет указать, работать ли с оригинальной или изменённой версией документа. |
| [Row](../com.aspose.words/row/) | Представляет строку таблицы. |
| [RowCollection](../com.aspose.words/rowcollection/) | Предоставляет типизированный доступ к коллекции узлов [Row](../com.aspose.words/row/). |
| [RowFormat](../com.aspose.words/rowformat/) | Представляет всё форматирование строки таблицы. |
| [RtfLoadOptions](../com.aspose.words/rtfloadoptions/) | Позволяет указать дополнительные параметры при загрузке документа [LoadFormat.\#RTF](../com.aspose.words/loadformat/\#RTF) в объект [Document](../com.aspose.words/document/). |
| [RtfSaveOptions](../com.aspose.words/rtfsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#RTF](../com.aspose.words/saveformat/\#RTF). |
| [Run](../com.aspose.words/run/) | Представляет последовательность символов с одинаковым форматированием шрифта. |
| [RunCollection](../com.aspose.words/runcollection/) | Обеспечивает типизированный доступ к коллекции узлов [Run](../com.aspose.words/run/). |
| [SaveFormat](../com.aspose.words/saveformat/) | Указывает формат, в котором сохраняется документ. |
| [SaveOptions](../com.aspose.words/saveoptions/) | Это абстрактный базовый класс для классов, позволяющих пользователю задавать дополнительные параметры при сохранении документа в определённый формат. |
| [SaveOutputParameters](../com.aspose.words/saveoutputparameters/) | Этот объект возвращается вызывающему после сохранения документа и содержит дополнительную информацию, которая была сгенерирована или вычислена во время операции сохранения. |
| [ScriptShapingLevel](../com.aspose.words/scriptshapinglevel/) | Описывает уровни формирования, требуемые скриптом. |
| [SdtAppearance](../com.aspose.words/sdtappearance/) | Указывает внешний вид структурированного тега документа. |
| [SdtCalendarType](../com.aspose.words/sdtcalendartype/) | Указывает возможные типы календарей, которые могут использоваться для задания [StructuredDocumentTag.\#getCalendarType()](../com.aspose.words/structureddocumenttag/\#getCalendarType) / [StructuredDocumentTag.\#setCalendarType(int)](../com.aspose.words/structureddocumenttag/\#setCalendarType-int) в документе Office Open XML. |
| [SdtDateStorageFormat](../com.aspose.words/sdtdatestorageformat/) | Указывает, как дата для SDT типа «date» хранится/извлекается, когда SDT привязан к узлу XML в хранилище данных документа. |
| [SdtListItem](../com.aspose.words/sdtlistitem/) | Этот элемент указывает отдельный элемент списка внутри родительского структурированного тега документа [SdtType.\#COMBO\_BOX](../com.aspose.words/sdttype/\#COMBO-BOX) или [SdtType.\#DROP\_DOWN\_LIST](../com.aspose.words/sdttype/\#DROP-DOWN-LIST). |
| [SdtListItemCollection](../com.aspose.words/sdtlistitemcollection/) | Обеспечивает доступ к элементам [SdtListItem](../com.aspose.words/sdtlistitem/) структурированного тега документа. |
| [SdtType](../com.aspose.words/sdttype/) | Указывает тип узла структурированного тега документа (SDT). |
| [Section](../com.aspose.words/section/) | Представляет отдельный раздел в документе. |
| [SectionCollection](../com.aspose.words/sectioncollection/) | Коллекция объектов [Section](../com.aspose.words/section/) в документе. |
| [SectionLayoutMode](../com.aspose.words/sectionlayoutmode/) | Указывает режим компоновки раздела, позволяющий задавать поведение сетки документа. |
| [SectionStart](../com.aspose.words/sectionstart/) | Тип разрыва в начале раздела. |
| [Shading](../com.aspose.words/shading/) | Содержит атрибуты затенения для объекта. |
| [ShadowFormat](../com.aspose.words/shadowformat/) | Представляет форматирование тени для объекта. |
| [ShadowType](../com.aspose.words/shadowtype/) | Указывает тип тени фигуры. |
| [Shape](../com.aspose.words/shape/) | Представляет объект в слое рисования, такой как AutoShape, текстовое поле, свободная форма, объект OLE, элемент управления ActiveX или изображение. |
| [ShapeBase](../com.aspose.words/shapebase/) | Базовый класс для объектов в слое рисования, таких как AutoShape, свободная форма, объект OLE, элемент управления ActiveX или изображение. |
| [ShapeLineStyle](../com.aspose.words/shapelinestyle/) | Указывает составной стиль линии объекта [Shape](../com.aspose.words/shape/). |
| [ShapeMarkupLanguage](../com.aspose.words/shapemarkuplanguage/) | Указывает язык разметки, используемый для фигуры. |
| [ShapeRenderer](../com.aspose.words/shaperenderer/) | Предоставляет методы для отрисовки отдельного [Shape](../com.aspose.words/shape/) или [GroupShape](../com.aspose.words/groupshape/) в растровое или векторное изображение или в объект Graphics. |
| [ShapeTextOrientation](../com.aspose.words/shapetextorientation/) | Указывает ориентацию текста в фигурах. |
| [ShapeType](../com.aspose.words/shapetype/) | Указывает тип фигуры в документе Microsoft Word. |
| [ShowInBalloons](../com.aspose.words/showinballoons/) | Указывает, какие версии отображаются в облачках. |
| [SignOptions](../com.aspose.words/signoptions/) | Позволяет указать параметры подписи документа. |
| [SignatureLine](../com.aspose.words/signatureline/) | Обеспечивает доступ к свойствам строки подписи. |
| [SignatureLineOptions](../com.aspose.words/signaturelineoptions/) | Позволяет указать параметры вставляемой строки подписи. |
| [SignerContext](../com.aspose.words/signercontext/) | Контекст подписанта документа. |
| [SmartTag](../com.aspose.words/smarttag/) | Этот элемент указывает наличие смарт-тега вокруг одной или нескольких встроенных структур (фрагментов, изображений, полей и т.д.) в абзаце. |
| [SoftEdgeFormat](../com.aspose.words/softedgeformat/) | Представляет форматирование мягкой границы для объекта. |
| [Source](../com.aspose.words/source/) | Представляет отдельный источник, такой как книга, статья в журнале или интервью. |
| [SourceType](../com.aspose.words/sourcetype/) | Представляет типы источников библиографии. |
| [SpecialChar](../com.aspose.words/specialchar/) | Базовый класс для специальных символов в документе. |
| [SplitCriteria](../com.aspose.words/splitcriteria/) | Указывает, как документ разбивается на части. |
| [SplitOptions](../com.aspose.words/splitoptions/) | Указывает параметры, как документ разбивается на части. |
| [Splitter](../com.aspose.words/splitter/) | Предоставляет методы, предназначенные для разбивки документов на части с использованием различных критериев. |
| [SplitterContext](../com.aspose.words/splittercontext/) | Контекст разделителя документа. |
| [Story](../com.aspose.words/story/) | Базовый класс для элементов, содержащих блоковые узлы [Paragraph](../com.aspose.words/paragraph/) и [Table](../com.aspose.words/table/). |
| [StoryType](../com.aspose.words/storytype/) | Текст документа Word хранится в историях. |
| [StreamFontSource](../com.aspose.words/streamfontsource/) | Базовый класс для пользовательского источника шрифтов из потока. |
| [Stroke](../com.aspose.words/stroke/) | Определяет обводку для фигуры. |
| [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/) | Представляет структурированный тег документа (SDT или элемент управления содержимым) в документе. |
| [StructuredDocumentTagCollection](../com.aspose.words/structureddocumenttagcollection/) | Коллекция экземпляров [IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag/), представляющих структурированные теги документа в указанном диапазоне. |
| [StructuredDocumentTagRangeEnd](../com.aspose.words/structureddocumenttagrangeend/) | Представляет конец **ranged** структурированного тега документа, который принимает содержимое из нескольких разделов. |
| [StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart/) | Представляет начало **ranged** структурированного тега документа, который принимает содержимое из нескольких разделов. |
| [Style](../com.aspose.words/style/) | Представляет один встроенный или пользовательский стиль. |
| [StyleCollection](../com.aspose.words/stylecollection/) | Коллекция объектов [Style](../com.aspose.words/style/), представляющих как встроенные, так и пользовательские стили в документе. |
| [StyleIdentifier](../com.aspose.words/styleidentifier/) | Идентификатор стиля, независимый от локали. |
| [StyleType](../com.aspose.words/styletype/) | Представляет тип стиля. |
| [SubDocument](../com.aspose.words/subdocument/) | Представляет **SubDocument** \- который является ссылкой на внешний документ. |
| [SummarizeOptions](../com.aspose.words/summarizeoptions/) | Позволяет указать различные параметры для суммирования содержимого документа. |
| [SummaryLength](../com.aspose.words/summarylength/) | Перечисляет возможные длины резюме. |
| [SuperUserJwtTokenRequestHandler](../com.aspose.words/superuserjwttokenrequesthandler/) | Обработчик запросов JWT‑токенов с кэшированием, локальной проверкой и автоматическим переключением. |
| [SvgSaveOptions](../com.aspose.words/svgsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#SVG](../com.aspose.words/saveformat/\#SVG). |
| [SvgTextOutputMode](../com.aspose.words/svgtextoutputmode/) | Позволяет указать, как текст внутри документа должен отображаться при сохранении в формате SVG. |
| [SystemFontSource](../com.aspose.words/systemfontsource/) | Представляет все шрифты TrueType, установленные в системе. |
| [TabAlignment](../com.aspose.words/tabalignment/) | Указывает выравнивание/тип табуляции. |
| [TabLeader](../com.aspose.words/tableader/) | Указывает тип линии‑заполнителя, отображаемой под символом табуляции. |
| [TabStop](../com.aspose.words/tabstop/) | Представляет одну пользовательскую табуляцию. |
| [TabStopCollection](../com.aspose.words/tabstopcollection/) | Коллекция объектов [TabStop](../com.aspose.words/tabstop/), представляющих пользовательские табуляции для абзаца или стиля. |
| [Table](../com.aspose.words/table/) | Представляет таблицу в документе Word. |
| [TableAlignment](../com.aspose.words/tablealignment/) | Указывает выравнивание встроенной таблицы. |
| [TableCollection](../com.aspose.words/tablecollection/) | Обеспечивает типизированный доступ к коллекции узлов [Table](../com.aspose.words/table/). |
| [TableContentAlignment](../com.aspose.words/tablecontentalignment/) | Позволяет указать выравнивание содержимого таблицы, используемое при экспорте в формат Markdown. |
| [TableStyle](../com.aspose.words/tablestyle/) | Представляет стиль таблицы. |
| [TableStyleOptions](../com.aspose.words/tablestyleoptions/) | Указывает, как стиль таблицы применяется к таблице. |
| [TableSubstitutionRule](../com.aspose.words/tablesubstitutionrule/) | Правило замены шрифтов в таблице. |
| [TaskPane](../com.aspose.words/taskpane/) | Представляет объект панели задач надстройки. |
| [TaskPaneCollection](../com.aspose.words/taskpanecollection/) | Указывает список сохранённых объектов панелей задач. |
| [TaskPaneDockState](../com.aspose.words/taskpanedockstate/) | Перечисляет доступные расположения объекта панели задач. |
| [TextBox](../com.aspose.words/textbox/) | Определяет атрибуты, указывающие, как текст отображается внутри фигуры. |
| [TextBoxAnchor](../com.aspose.words/textboxanchor/) | Указывает значения, используемые для вертикального выравнивания текста в фигуре. |
| [TextBoxControl](../com.aspose.words/textboxcontrol/) | Элемент управления TextBox отображает текст из упорядоченного набора данных или ввода пользователя. |
| [TextBoxWrapMode](../com.aspose.words/textboxwrapmode/) | Указывает, как текст обтекает форму. |
| [TextColumn](../com.aspose.words/textcolumn/) | Представляет одну колонку текста. |
| [TextColumnCollection](../com.aspose.words/textcolumncollection/) | Коллекция объектов [TextColumn](../com.aspose.words/textcolumn/), представляющих все колонки текста в разделе документа. |
| [TextDmlEffect](../com.aspose.words/textdmleffect/) | Эффект DML текста для последовательностей текста. |
| [TextEffect](../com.aspose.words/texteffect/) | Эффект анимации для последовательностей текста. |
| [TextFormFieldType](../com.aspose.words/textformfieldtype/) | Указывает тип текстового поля формы. |
| [TextOrientation](../com.aspose.words/textorientation/) | Указывает ориентацию текста на странице, в ячейке таблицы или в текстовой рамке. |
| [TextPath](../com.aspose.words/textpath/) | Определяет текст и форматирование текстовой траектории (объекта WordArt). |
| [TextPathAlignment](../com.aspose.words/textpathalignment/) | Выравнивание WordArt. |
| [TextWatermarkOptions](../com.aspose.words/textwatermarkoptions/) | Содержит параметры, которые можно указать при добавлении водяного знака с текстом. |
| [TextWrapping](../com.aspose.words/textwrapping/) | Указывает, как текст обтекает таблицу. |
| [TextureAlignment](../com.aspose.words/texturealignment/) | Указывает выравнивание при черепичной заливке текстурой. |
| [TextureIndex](../com.aspose.words/textureindex/) | Указывает текстуру затенения. |
| [Theme](../com.aspose.words/theme/) | Представляет тему документа и предоставляет доступ к основным частям темы, включая [Theme.\#getMajorFonts()](../com.aspose.words/theme/\#getMajorFonts), [Theme.\#getMinorFonts()](../com.aspose.words/theme/\#getMinorFonts) и [Theme.\#getColors()](../com.aspose.words/theme/\#getColors) |
| [ThemeColor](../com.aspose.words/themecolor/) | Указывает цвета темы для тем документа. |
| [ThemeColors](../com.aspose.words/themecolors/) | Представляет цветовую схему темы документа, содержащую двенадцать цветов. |
| [ThemeFont](../com.aspose.words/themefont/) | Указывает типы названий шрифтов темы для тем документа. |
| [ThemeFonts](../com.aspose.words/themefonts/) | Представляет коллекцию шрифтов в схеме шрифтов, позволяя указывать разные шрифты для разных языков [ThemeFonts.\#getLatin()](../com.aspose.words/themefonts/\#getLatin) / [ThemeFonts.\#setLatin(java.lang.String)](../com.aspose.words/themefonts/\#setLatin-java.lang.String), [ThemeFonts.\#getEastAsian()](../com.aspose.words/themefonts/\#getEastAsian) / [ThemeFonts.\#setEastAsian(java.lang.String)](../com.aspose.words/themefonts/\#setEastAsian-java.lang.String) и [ThemeFonts.\#getComplexScript()](../com.aspose.words/themefonts/\#getComplexScript) / [ThemeFonts.\#setComplexScript(java.lang.String)](../com.aspose.words/themefonts/\#setComplexScript-java.lang.String). |
| [ThumbnailGeneratingOptions](../com.aspose.words/thumbnailgeneratingoptions/) | Можно использовать для указания дополнительных параметров при создании миниатюры документа. |
| [TiffCompression](../com.aspose.words/tiffcompression/) | Указывает тип сжатия, применяемый при сохранении изображений страниц в файл TIFF. |
| [ToaCategories](../com.aspose.words/toacategories/) | Представляет таблицу категорий авторитетов. |
| [TxtExportHeadersFootersMode](../com.aspose.words/txtexportheadersfootersmode/) | Указывает способ экспорта верхних и нижних колонтитулов в формат простого текста. |
| [TxtLeadingSpacesOptions](../com.aspose.words/txtleadingspacesoptions/) | Указывает доступные параметры обработки начальных пробелов при импорте из файла [LoadFormat.\#TEXT](../com.aspose.words/loadformat/\#TEXT). |
| [TxtListIndentation](../com.aspose.words/txtlistindentation/) | Указывает, как уровни списка отступают при экспорте документа в формат [SaveFormat.\#TEXT](../com.aspose.words/saveformat/\#TEXT). |
| [TxtLoadOptions](../com.aspose.words/txtloadoptions/) | Позволяет указать дополнительные параметры при загрузке документа [LoadFormat.\#TEXT](../com.aspose.words/loadformat/\#TEXT) в объект [Document](../com.aspose.words/document/). |
| [TxtOfficeMathExportMode](../com.aspose.words/txtofficemathexportmode/) | Указывает, как Aspose.Words экспортирует OfficeMath в [SaveFormat.\#TEXT](../com.aspose.words/saveformat/\#TEXT). |
| [TxtSaveOptions](../com.aspose.words/txtsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#TEXT](../com.aspose.words/saveformat/\#TEXT). |
| [TxtSaveOptionsBase](../com.aspose.words/txtsaveoptionsbase/) | Базовый класс для указания дополнительных параметров при сохранении документа в текстовые форматы. |
| [TxtTrailingSpacesOptions](../com.aspose.words/txttrailingspacesoptions/) | Указывает доступные параметры обработки конечных пробелов при импорте из файла [LoadFormat.\#TEXT](../com.aspose.words/loadformat/\#TEXT). |
| [Underline](../com.aspose.words/underline/) | Указывает тип подчеркивания, применяемого к шрифту. |
| [UnicodeScript](../com.aspose.words/unicodescript/) | Свойство базы данных символов Unicode: Script (sc). |
| [UnsupportedEncryptionException](../com.aspose.words/unsupportedencryptionexception/) | Выбрасывается при загрузке документа, когда документ зашифрован неподдерживаемым методом. |
| [UnsupportedFileFormatException](../com.aspose.words/unsupportedfileformatexception/) | Выбрасывается при загрузке документа, когда формат документа не распознан или не поддерживается Aspose.Words. |
| [UserInformation](../com.aspose.words/userinformation/) | Указывает информацию о пользователе. |
| [VariableCollection](../com.aspose.words/variablecollection/) | Коллекция переменных документа. |
| [VariationAxis](../com.aspose.words/variationaxis/) | Представляет тег оси вариаций дизайна OpenType. |
| [VariationAxisCoordinate](../com.aspose.words/variationaxiscoordinate/) | Представляет координату оси. |
| [VbaModule](../com.aspose.words/vbamodule/) | Обеспечивает доступ к модулю проекта VBA. |
| [VbaModuleCollection](../com.aspose.words/vbamodulecollection/) | Представляет коллекцию объектов [VbaModule](../com.aspose.words/vbamodule/). |
| [VbaModuleType](../com.aspose.words/vbamoduletype/) | Указывает тип модели в проекте VBA. |
| [VbaProject](../com.aspose.words/vbaproject/) | Обеспечивает доступ к информации проекта VBA. |
| [VbaReference](../com.aspose.words/vbareference/) | Реализует ссылку на библиотеку типов Automation или проект VBA. |
| [VbaReferenceCollection](../com.aspose.words/vbareferencecollection/) | Представляет коллекцию объектов [VbaReference](../com.aspose.words/vbareference/). |
| [VbaReferenceType](../com.aspose.words/vbareferencetype/) | Позволяет указать тип объекта [VbaReference](../com.aspose.words/vbareference/). |
| [VerticalAlignment](../com.aspose.words/verticalalignment/) | Указывает вертикальное выравнивание плавающей фигуры, текстового фрейма или плавающей таблицы. |
| [ViewOptions](../com.aspose.words/viewoptions/) | Предоставляет различные параметры, контролирующие отображение документа в Microsoft Word. |
| [ViewType](../com.aspose.words/viewtype/) | Возможные значения режима просмотра в Microsoft Word. |
| [VisitorAction](../com.aspose.words/visitoraction/) | Позволяет посетителю управлять перечислением узлов. |
| [WarningInfo](../com.aspose.words/warninginfo/) | Содержит информацию о предупреждении, выданном Aspose.Words во время загрузки или сохранения документа. |
| [WarningInfoCollection](../com.aspose.words/warninginfocollection/) | Представляет типизированную коллекцию объектов [WarningInfo](../com.aspose.words/warninginfo/). |
| [WarningSource](../com.aspose.words/warningsource/) | Указывает модуль, который генерирует предупреждение при загрузке или сохранении документа. |
| [WarningType](../com.aspose.words/warningtype/) | Указывает тип предупреждения, выдаваемого Aspose.Words при загрузке или сохранении документа. |
| [Watermark](../com.aspose.words/watermark/) | Представляет класс для работы с водяным знаком документа. |
| [WatermarkLayout](../com.aspose.words/watermarklayout/) | Определяет расположение водяного знака относительно его центра. |
| [WatermarkType](../com.aspose.words/watermarktype/) | Указывает тип водяного знака. |
| [Watermarker](../com.aspose.words/watermarker/) | Предоставляет методы, предназначенные для вставки водяных знаков в документы. |
| [WatermarkerContext](../com.aspose.words/watermarkercontext/) | Контекст водяного знака документа. |
| [WebExtension](../com.aspose.words/webextension/) | Представляет объект веб‑расширения. |
| [WebExtensionBinding](../com.aspose.words/webextensionbinding/) | Указывает связь привязки между веб‑расширением и данными в документе. |
| [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection/) | Указывает список привязок веб‑расширения. |
| [WebExtensionBindingType](../com.aspose.words/webextensionbindingtype/) | Перечисляет доступные типы привязки между веб‑расширением и данными в документе. |
| [WebExtensionProperty](../com.aspose.words/webextensionproperty/) | Указывает пользовательское свойство веб‑расширения. |
| [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection/) | Указывает набор пользовательских свойств веб‑расширения. |
| [WebExtensionReference](../com.aspose.words/webextensionreference/) | Представляет ссылку на веб‑расширение. |
| [WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection/) | Указывает список ссылок на веб‑расширения. |
| [WebExtensionStoreType](../com.aspose.words/webextensionstoretype/) | Перечисляет доступные типы хранилища веб‑расширения. |
| [WordML2003SaveOptions](../com.aspose.words/wordml2003saveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#WORD\_ML](../com.aspose.words/saveformat/\#WORD-ML). |
| [WrapSide](../com.aspose.words/wrapside/) | Указывает, с какой стороны(сторон) формы или изображения обтекает текст. |
| [WrapType](../com.aspose.words/wraptype/) | Указывает, как текст обтекает форму или изображение. |
| [WriteProtection](../com.aspose.words/writeprotection/) | Указывает настройки защиты от записи для документа. |
| [X509Certificate2Wrapper](../com.aspose.words/x509certificate2wrapper/) | Публичный обёртка, добавленная в JAVA, вокруг нашего внутреннего X509Certificate2. |
| [XamlFixedSaveOptions](../com.aspose.words/xamlfixedsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#XAML\_FIXED](../com.aspose.words/saveformat/\#XAML-FIXED). |
| [XamlFlowSaveOptions](../com.aspose.words/xamlflowsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#XAML\_FLOW](../com.aspose.words/saveformat/\#XAML-FLOW) или [SaveFormat.\#XAML\_FLOW\_PACK](../com.aspose.words/saveformat/\#XAML-FLOW-PACK). |
| [XlsxDateTimeParsingMode](../com.aspose.words/xlsxdatetimeparsingmode/) | Указывает, как текст документа анализируется для определения значений даты и времени. |
| [XlsxSaveOptions](../com.aspose.words/xlsxsaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#XLSX](../com.aspose.words/saveformat/\#XLSX). |
| [XlsxSectionMode](../com.aspose.words/xlsxsectionmode/) | Указывает, как обрабатываются разделы при сохранении документа в формате XLSX. |
| [XmlDataLoadOptions](../com.aspose.words/xmldataloadoptions/) | Представляет параметры загрузки XML-данных. |
| [XmlDataSource](../com.aspose.words/xmldatasource/) | Обеспечивает доступ к данным XML‑файла или потока, которые будут использоваться в отчёте. |
| [XmlDsigLevel](../com.aspose.words/xmldsiglevel/) | Указывает уровень цифровой подписи в соответствии со стандартом XML-DSig. |
| [XmlMapping](../com.aspose.words/xmlmapping/) | Указывает информацию, используемую для установления сопоставления между родительским тегом структурированного документа и элементом XML, хранящимся в пользовательской части XML‑данных документа. |
| [XpsSaveOptions](../com.aspose.words/xpssaveoptions/) | Можно использовать для указания дополнительных параметров при сохранении документа в формат [SaveFormat.\#XPS](../com.aspose.words/saveformat/\#XPS). |
| [Zip64Mode](../com.aspose.words/zip64mode/) | Указывает, когда использовать расширения формата ZIP64 для файлов OOXML. |
| [ZoomType](../com.aspose.words/zoomtype/) | Возможные значения того, насколько большой или маленький документ отображается на экране в Microsoft Word. |

## Интерфейсы

| Интерфейс | Описание |
| --- | --- |
| [IBarcodeGenerator](../com.aspose.words/ibarcodegenerator/) | Публичный интерфейс для пользовательского генератора штрих‑кодов. |
| [IBibliographyStylesProvider](../com.aspose.words/ibibliographystylesprovider/) | Реализуйте этот интерфейс, чтобы предоставить стиль библиографии для полей [FieldBibliography](../com.aspose.words/fieldbibliography/) и [FieldCitation](../com.aspose.words/fieldcitation/) при их обновлении. |
| [IChartDataPoint](../com.aspose.words/ichartdatapoint/) | Содержит свойства отдельной точки данных на диаграмме. |
| [IComparisonExpressionEvaluator](../com.aspose.words/icomparisonexpressionevaluator/) | При реализации позволяет переопределить оценку выражений сравнения по умолчанию для полей [FieldIf](../com.aspose.words/fieldif/) и [FieldCompare](../com.aspose.words/fieldcompare/). |
| [ICssSavingCallback](../com.aspose.words/icsssavingcallback/) | Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет CSS (Cascading Style Sheet) при сохранении документа в HTML. |
| [IDocumentConverterPlugin](../com.aspose.words/idocumentconverterplugin/) | Определяет интерфейс для внешнего плагина конвертера. |
| [IDocumentLoadingCallback](../com.aspose.words/idocumentloadingcallback/) | Реализуйте этот интерфейс, если хотите иметь собственный пользовательский метод, вызываемый при загрузке документа. |
| [IDocumentMergerPlugin](../com.aspose.words/idocumentmergerplugin/) | Определяет интерфейс для внешнего плагина слияния, который может объединять PDF‑документы. |
| [IDocumentPartSavingCallback](../com.aspose.words/idocumentpartsavingcallback/) | Реализуйте этот интерфейс, если хотите получать уведомления и контролировать, как Aspose.Words сохраняет части документа при экспорте в формат [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML) или [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB). |
| [IDocumentProcessorPlugin](../com.aspose.words/idocumentprocessorplugin/) | Определяет интерфейс для внешнего плагина обработки документов. |
| [IDocumentReaderPlugin](../com.aspose.words/idocumentreaderplugin/) | Определяет интерфейс для внешних плагинов‑чтения, которые могут читать файл в документ. |
| [IDocumentSavingCallback](../com.aspose.words/idocumentsavingcallback/) | Реализуйте этот интерфейс, если хотите иметь собственный пользовательский метод, вызываемый при сохранении документа. |
| [IFieldDatabaseProvider](../com.aspose.words/ifielddatabaseprovider/) | Реализуйте этот интерфейс, чтобы предоставить данные для поля [FieldDatabase](../com.aspose.words/fielddatabase/) при его обновлении. |
| [IFieldMergingCallback](../com.aspose.words/ifieldmergingcallback/) | Реализуйте этот интерфейс, если хотите контролировать, как данные вставляются в поля слияния во время операции слияния почты. |
| [IFieldResultFormatter](../com.aspose.words/ifieldresultformatter/) | Реализуйте этот интерфейс, если хотите контролировать, как форматируется результат поля. |
| [IFieldUpdateCultureProvider](../com.aspose.words/ifieldupdatecultureprovider/) | При реализации предоставляет объект [CultureInfo](../com.aspose.words.net.system.globalization/cultureinfo/), который следует использовать во время обновления конкретного поля. |
| [IFieldUpdatingCallback](../com.aspose.words/ifieldupdatingcallback/) | Реализуйте этот интерфейс, если вы хотите иметь собственные пользовательские методы, вызываемые во время обновления поля. |
| [IFieldUpdatingProgressCallback](../com.aspose.words/ifieldupdatingprogresscallback/) | Реализуйте этот интерфейс, если вы хотите отслеживать прогресс обновления поля. |
| [IFieldUserPromptRespondent](../com.aspose.words/ifielduserpromptrespondent/) | Представляет ответчика на запросы пользователя во время обновления поля. |
| [IFontSavingCallback](../com.aspose.words/ifontsavingcallback/) | Реализуйте этот интерфейс, если вы хотите получать уведомления и контролировать, как Aspose.Words сохраняет шрифты при экспорте документа в формат HTML. |
| [IHyphenationCallback](../com.aspose.words/ihyphenationcallback/) | Реализуется классами, которые могут регистрировать словари переносов. |
| [IImageSavingCallback](../com.aspose.words/iimagesavingcallback/) | Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет изображения при сохранении документа в HTML. |
| [IIndexFilter](../com.aspose.words/iindexfilter/) | Определяет фильтр для пропуска элементов на основе их индексов. |
| [IMailMergeCallback](../com.aspose.words/imailmergecallback/) | Реализуйте этот интерфейс, если вы хотите получать уведомления во время выполнения слияния почты. |
| [IMailMergeDataSource](../com.aspose.words/imailmergedatasource/) | Реализуйте этот интерфейс, чтобы разрешить слияние почты из пользовательского источника данных, например списка объектов. |
| [IMailMergeDataSourceRoot](../com.aspose.words/imailmergedatasourceroot/) | Реализуйте этот интерфейс, чтобы разрешить слияние почты из пользовательского источника данных с данными мастер‑деталь. |
| [INodeChangingCallback](../com.aspose.words/inodechangingcallback/) | Реализуйте этот интерфейс, если вы хотите получать уведомления, когда узлы вставляются или удаляются в документе. |
| [IPageLayoutCallback](../com.aspose.words/ipagelayoutcallback/) | Реализуйте этот интерфейс, если вы хотите иметь собственный пользовательский метод, вызываемый во время построения и рендеринга модели разметки страницы. |
| [IPageSavingCallback](../com.aspose.words/ipagesavingcallback/) | Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет отдельные страницы при сохранении документа в фиксированные форматы страниц. |
| [IReplacingCallback](../com.aspose.words/ireplacingcallback/) | Реализуйте этот интерфейс, если вы хотите иметь собственный пользовательский метод, вызываемый во время операции поиска и замены. |
| [IResourceLoadingCallback](../com.aspose.words/iresourceloadingcallback/) | Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words загружает внешние ресурсы при импорте документа и вставке изображений с помощью [DocumentBuilder](../com.aspose.words/documentbuilder/). |
| [IResourceSavingCallback](../com.aspose.words/iresourcesavingcallback/) | Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет внешние ресурсы (изображения, шрифты и CSS) при сохранении документа в фиксированный HTML или SVG. |
| [IRevisionCriteria](../com.aspose.words/irevisioncriteria/) | Реализуйте этот интерфейс, если вы хотите контролировать, когда определённые [Revision](../com.aspose.words/revision/) должны быть приняты/отклонены или нет методами [RevisionCollection.\#accept(com.aspose.words.IRevisionCriteria)](../com.aspose.words/revisioncollection/\#accept-com.aspose.words.IRevisionCriteria)/ [RevisionCollection.\#reject(com.aspose.words.IRevisionCriteria)](../com.aspose.words/revisioncollection/\#reject-com.aspose.words.IRevisionCriteria). |
| [IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag/) | Интерфейс для определения общих данных для [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/) и [StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart/). |
| [ITextShaper](../com.aspose.words/itextshaper/) | Предоставляет методы для формирования текста. |
| [ITextShaperFactory](../com.aspose.words/itextshaperfactory/) | Интерфейс фабрики для создания реализаций [ITextShaper](../com.aspose.words/itextshaper/). |
| [IWarningCallback](../com.aspose.words/iwarningcallback/) | Реализуйте этот интерфейс, если вы хотите иметь собственный пользовательский метод, вызываемый для захвата предупреждений о потере точности, которые могут возникнуть при загрузке или сохранении документа. |
