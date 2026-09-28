---
title: "Класс Aspose::Words::Document"
linktitle: "Document"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Document. Представляет документ Word. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words/document/
---
## Document class


Представляет документ Word. Чтобы узнать больше, посетите статью документации [Working with Document](https://docs.aspose.com/words/cpp/working-with-document/).

```cpp
class Document : public Aspose::Words::DocumentBase,
                 public Aspose::Words::ISectionAttrSource,
                 public Aspose::Words::IWatermarkProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [AcceptAllRevisions](./acceptallrevisions/)() | Принимает все отслеживаемые изменения в документе. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для обхода конца документа. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для обхода начала документа. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Добавляет указанный документ в конец этого документа. |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Добавляет указанный документ в конец этого документа. |
| [Cleanup](./cleanup/)() | Очищает документ от неиспользуемых стилей и списков. |
| [Cleanup](./cleanup/)(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) | Очищает документ от неиспользуемых стилей и списков в зависимости от заданных [CleanupOptions](../cleanupoptions/). |
| [Clone](./clone/)() | Выполняет глубокое копирование [Document](./). |
| [Clone](../node/clone/)(bool) | Создаёт дубликат узла. |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime) | Сравнивает этот документ с другим документом, создавая изменения в виде количества правок и форматных ревизий [Revision](../revision/). |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Сравнивает этот документ с другим документом, создавая изменения в виде количества правок и форматных ревизий [Revision](../revision/). Позволяет задавать параметры сравнения с помощью [CompareOptions](../../aspose.words.comparing/compareoptions/). |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::String\&) | Копирует стили из указанного шаблона в документ. |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Копирует стили из указанного шаблона в документ. |
| [Document](./document/)() | Создаёт пустой документ Word. |
| [Document](./document/)(const System::String\&) | Открывает существующий документ из файла. Автоматически определяет формат файла. |
| [Document](./document/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Открывает существующий документ из файла. Позволяет указывать дополнительные параметры, такие как пароль шифрования. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&) | Открывает существующий документ из потока. Автоматически определяет формат файла. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Открывает существующий документ из потока. Позволяет указывать дополнительные параметры, такие как пароль шифрования. |
| [Document](./document/)(std::istream\&) |  |
| [Document](./document/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| [EnsureMinimum](./ensureminimum/)() | Если документ не содержит разделов, создаёт один раздел с одним абзацем. |
| [ExpandTableStylesToDirectFormatting](./expandtablestylestodirectformatting/)() | Преобразует форматирование, указанное в стилях таблиц, в прямое форматирование таблиц в документе. |
| [ExtractPages](./extractpages/)(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) | Возвращает объект [Document](./), представляющий указанный диапазон страниц и заданные параметры извлечения страниц. |
| [ExtractPages](./extractpages/)(int32_t, int32_t) | Возвращает объект [Document](./), представляющий указанный диапазон страниц. |
| [get_AttachedTemplate](./get_attachedtemplate/)() | Получает или задаёт полный путь к шаблону, прикреплённому к документу. |
| [get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/)() | Получает или задаёт флаг, указывающий, обновляются ли стили в документе для соответствия стилям прикреплённого шаблона каждый раз при открытии документа в MS Word. |
| [get_BackgroundShape](../documentbase/get_backgroundshape/)() const | Получает или задает форму фона документа. Может быть **null**. |
| [get_Bibliography](./get_bibliography/)() | Получает объект [Bibliography](./get_bibliography/), который представляет список источников, доступных в документе. |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Возвращает коллекцию, представляющую все встроенные свойства документа. |
| [get_CompatibilityOptions](./get_compatibilityoptions/)() | Обеспечивает доступ к параметрам совместимости документа (то есть к пользовательским настройкам, введённым на вкладке **Compatibility** диалогового окна **Options** в Word). |
| [get_Compliance](./get_compliance/)() | Получает версию соответствия OOXML, определённую из содержимого загруженного документа. Имеет смысл только для документов OOXML. |
| [get_Count](../compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() | Возвращает коллекцию, представляющую все пользовательские свойства документа. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| [get_CustomXmlParts](./get_customxmlparts/)() const | Получает или задает коллекцию частей хранилища пользовательских XML‑данных. |
| [get_DefaultTabStop](./get_defaulttabstop/)() | Получает или задает интервал (в пунктах) между стандартными табуляциями. |
| [get_DigitalSignatures](./get_digitalsignatures/)() const | Получает коллекцию цифровых подписей этого документа и их результаты проверки. |
| [get_Document](../documentbase/get_document/)() const override | Получает текущий экземпляр. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Предоставляет параметры, управляющие нумерацией и размещением концевых сносок в этом документе. |
| [get_FieldOptions](./get_fieldoptions/)() | Получает объект [FieldOptions](../../aspose.words.fields/fieldoptions/), представляющий параметры управления обработкой полей в документе. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_FirstSection](./get_firstsection/)() | Получает первый раздел в документе. |
| [get_FontInfos](../documentbase/get_fontinfos/)() const | Обеспечивает доступ к свойствам шрифтов, используемых в этом документе. |
| [get_FontSettings](./get_fontsettings/)() const | Получает или задает настройки шрифтов документа. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Предоставляет параметры, управляющие нумерацией и размещением сносок в этом документе. |
| [get_FootnoteSeparators](../documentbase/get_footnoteseparators/)() const | Обеспечивает доступ к разделителям сносок/концевых сносок, определённым в документе. |
| [get_Frameset](./get_frameset/)() const | Возвращает экземпляр [Frameset](./get_frameset/), если этот документ представляет страницу с фреймами. |
| [get_GlossaryDocument](./get_glossarydocument/)() const | Получает или задает глоссарий внутри этого документа или шаблона. Глоссарий — это хранилище записей AutoText, AutoCorrect и Building Block, определённых в документе. |
| [get_GrammarChecked](./get_grammarchecked/)() | Возвращает **true**, если документ был проверен на грамматику. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_HasMacros](./get_hasmacros/)() | Возвращает **true**, если в документе есть проект VBA (макросы). |
| [get_HasRevisions](./get_hasrevisions/)() | Возвращает **true**, если в документе есть отслеживаемые изменения. |
| [get_HyphenationOptions](./get_hyphenationoptions/)() | Обеспечивает доступ к параметрам переноса слов в документе. |
| [get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/)() | Указывает, включать ли текстовые поля, сноски и концевые сноски в статистику подсчёта слов. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_JustificationMode](./get_justificationmode/)() | Получает или задает корректировку межсимвольного интервала документа. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_LastSection](./get_lastsection/)() | Получает последний раздел в документе. |
| [get_LayoutOptions](./get_layoutoptions/)() const | Получает объект [LayoutOptions](../../aspose.words.layout/layoutoptions/), который представляет параметры управления процессом компоновки этого документа. |
| [get_Lists](../documentbase/get_lists/)() const | Предоставляет доступ к форматированию списков, используемому в документе. |
| [get_MailMerge](./get_mailmerge/)() | Возвращает объект [MailMerge](../../aspose.words.mailmerging/mailmerge/), который представляет функциональность слияния почты для документа. |
| [get_MailMergeSettings](./get_mailmergesettings/)() | Получает или задает объект, содержащий всю информацию о слиянии почты для документа. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeChangingCallback](../documentbase/get_nodechangingcallback/)() | Вызывается, когда узел вставляется или удаляется в документе. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает [Document](../nodetype/). |
| [get_OriginalFileName](./get_originalfilename/)() const | Получает исходное имя файла документа. |
| [get_OriginalLoadFormat](./get_originalloadformat/)() const | Получает формат исходного документа, загруженного в этот объект. |
| [get_PackageCustomParts](./get_packagecustomparts/)() const | Получает или задает коллекцию пользовательских частей (произвольного содержимого), связанных с пакетом OOXML с помощью «неизвестных связей». |
| [get_PageColor](../documentbase/get_pagecolor/)() | Получает или задает цвет страницы документа. Это свойство является упрощённой версией [BackgroundShape](../documentbase/get_backgroundshape/). |
| [get_PageCount](./get_pagecount/)() | Получает количество страниц в документе, рассчитанное последней операцией компоновки страниц. |
| [get_ParentNode](../node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectionType](./get_protectiontype/)() | Получает текущий активный тип защиты документа. |
| [get_PunctuationKerning](./get_punctuationkerning/)() | Указывает, применяется ли кернинг к латинскому тексту и пунктуации. |
| [get_Range](../node/get_range/)() | Возвращает объект [Range](../range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_ReadabilityStatistics](./get_readabilitystatistics/)() | Предоставляет информацию о показателе читаемости документа. |
| [get_RemovePersonalInformation](./get_removepersonalinformation/)() | Получает или задает флаг, указывающий, что Microsoft Word будет удалять всю пользовательскую информацию из комментариев, правок и свойств документа при сохранении. |
| [get_ResourceLoadingCallback](../documentbase/get_resourceloadingcallback/)() const | Позволяет управлять тем, как загружаются внешние ресурсы. |
| [get_Revisions](./get_revisions/)() | Получает коллекцию ревизий (отслеживаемых изменений), существующих в этом документе. |
| [get_RevisionsView](./get_revisionsview/)() const | Получает или задает значение, указывающее, работать ли с оригинальной или исправленной версией документа. |
| [get_Sections](./get_sections/)() | Возвращает коллекцию, представляющую все разделы в документе. |
| [get_ShadeFormData](./get_shadeformdata/)() | Указывает, включать ли серую заливку в полях формы. |
| [get_ShowGrammaticalErrors](./get_showgrammaticalerrors/)() | Указывает, отображать ли грамматические ошибки в этом документе. |
| [get_ShowSpellingErrors](./get_showspellingerrors/)() | Указывает, отображать ли орфографические ошибки в этом документе. |
| [get_SpellingChecked](./get_spellingchecked/)() | Возвращает **true**, если документ был проверен на орфографию. |
| [get_Styles](../documentbase/get_styles/)() const | Возвращает коллекцию стилей, определённых в документе. |
| [get_Theme](./get_theme/)() | Получает объект [Theme](./get_theme/) для этого документа. |
| [get_TrackRevisions](./get_trackrevisions/)() | True, если изменения отслеживаются, когда этот документ редактируется в Microsoft Word. |
| [get_Variables](./get_variables/)() | Возвращает коллекцию переменных, добавленных в документ или шаблон. |
| [get_VbaProject](./get_vbaproject/)() const | Получает или задает [VbaProject](./get_vbaproject/). |
| [get_VersionsCount](./get_versionscount/)() | Получает количество версий документа, сохранённых в DOC‑документе. |
| [get_ViewOptions](./get_viewoptions/)() | Предоставляет параметры для управления тем, как документ отображается в Microsoft Word. |
| [get_WarningCallback](../documentbase/get_warningcallback/)() const | Вызывается во время различных процедур обработки документа, когда обнаруживается проблема, которая может привести к потере точности данных или форматирования. |
| [get_Watermark](./get_watermark/)() | Предоставляет доступ к водяному знаку документа. |
| [get_WebExtensionTaskPanes](./get_webextensiontaskpanes/)() const | Возвращает коллекцию, представляющую список надстроек панели задач. |
| [get_WriteProtection](./get_writeprotection/)() | Предоставляет доступ к параметрам защиты документа от записи. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Получает первого предка указанного [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Возвращает N‑й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Обеспечивает поддержку итерации в стиле foreach по дочерним узлам этого узла. |
| [GetPageInfo](./getpageinfo/)(int32_t) | Получает размер страницы, ориентацию и другую информацию о странице, которая может быть полезна для печати или визуализации. |
| [GetText](../compositenode/gettext/)() override | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Импортирует узел из другого документа в текущий документ. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Импортирует узел из другого документа в текущий документ с параметром для управления форматированием. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Импортирует узел из другого документа в текущий документ с параметром для управления форматированием. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Объединяет последовательности с одинаковым форматированием во всех абзацах документа. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Изменяет значения типа поля [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) у [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) во всём документе, чтобы они соответствовали типам полей, содержащимся в кодах полей. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Protect](./protect/)(Aspose::Words::ProtectionType) | Защищает документ от изменений без изменения существующего пароля или назначает случайный пароль. |
| [Protect](./protect/)(Aspose::Words::ProtectionType, const System::String\&) | Защищает документ от изменений и при желании задаёт пароль защиты. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveBlankPages](./removeblankpages/)() | Удаляет пустые страницы из документа. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveCustomizations](./removecustomizations/)() | Удаляет настройки панелей инструментов и клавиатурных команд из документа. |
| [RemoveExternalSchemaReferences](./removeexternalschemareferences/)() | Удаляет внешние ссылки на XML‑схемы из этого документа. |
| [RemoveMacros](./removemacros/)() | Удаляет все макросы (VBA‑проект), а также панели инструментов и настройки команд из документа. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Удаляет все дочерние узлы [SmartTag](../../aspose.words.markup/smarttag/) текущего узла. |
| [RenderToScale](./rendertoscale/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Отрисовывает страницу документа в объект **Graphics** с указанным масштабом. |
| [RenderToSize](./rendertosize/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Отрисовывает страницу документа в объект **Graphics** с указанным размером. |
| [Save](./save/)(const System::String\&) | Сохраняет документ в файл. Автоматически определяет формат сохранения по расширению. |
| [Save](./save/)(const System::String\&, Aspose::Words::SaveFormat) | Сохраняет документ в файл в указанном формате. |
| [Save](./save/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Сохраняет документ в файл, используя указанные параметры сохранения. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Сохраняет документ в поток, используя указанный формат. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Сохраняет документ в поток, используя указанные параметры сохранения. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) |  |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Выбирает список узлов, соответствующих XPath-выражению. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Выбирает первый [Node](../node/), который соответствует выражению XPath. |
| [set_AttachedTemplate](./set_attachedtemplate/)(const System::String\&) | Сеттер для [Aspose::Words::Document::get_AttachedTemplate](./get_attachedtemplate/). |
| [set_AutomaticallyUpdateStyles](./set_automaticallyupdatestyles/)(bool) | Сеттер для [Aspose::Words::Document::get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/). |
| [set_BackgroundShape](../documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Сеттер для [Aspose::Words::DocumentBase::get_BackgroundShape](../documentbase/get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_CustomXmlParts](./set_customxmlparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPartCollection\>\&) | Сеттер для [Aspose::Words::Document::get_CustomXmlParts](./get_customxmlparts/). |
| [set_DefaultTabStop](./set_defaulttabstop/)(double) | Сеттер для [Aspose::Words::Document::get_DefaultTabStop](./get_defaulttabstop/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Сеттер для [Aspose::Words::Document::get_FontSettings](./get_fontsettings/). |
| [set_GlossaryDocument](./set_glossarydocument/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | Сеттер для [Aspose::Words::Document::get_GlossaryDocument](./get_glossarydocument/). |
| [set_GrammarChecked](./set_grammarchecked/)(bool) | Сеттер для [Aspose::Words::Document::get_GrammarChecked](./get_grammarchecked/). |
| [set_IncludeTextboxesFootnotesEndnotesInStat](./set_includetextboxesfootnotesendnotesinstat/)(bool) | Сеттер для [Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/). |
| [set_JustificationMode](./set_justificationmode/)(Aspose::Words::Settings::JustificationMode) | Сеттер для [Aspose::Words::Document::get_JustificationMode](./get_justificationmode/). |
| [set_MailMergeSettings](./set_mailmergesettings/)(const System::SharedPtr\<Aspose::Words::Settings::MailMergeSettings\>\&) | Сеттер для [Aspose::Words::Document::get_MailMergeSettings](./get_mailmergesettings/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Вызывается, когда узел вставляется или удаляется в документе. |
| [set_PackageCustomParts](./set_packagecustomparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPartCollection\>\&) | Сеттер для [Aspose::Words::Document::get_PackageCustomParts](./get_packagecustomparts/). |
| [set_PageColor](../documentbase/set_pagecolor/)(System::Drawing::Color) | Сеттер для [Aspose::Words::DocumentBase::get_PageColor](../documentbase/get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PunctuationKerning](./set_punctuationkerning/)(bool) | Сеттер для [Aspose::Words::Document::get_PunctuationKerning](./get_punctuationkerning/). |
| [set_RemovePersonalInformation](./set_removepersonalinformation/)(bool) | Сеттер для [Aspose::Words::Document::get_RemovePersonalInformation](./get_removepersonalinformation/). |
| [set_ResourceLoadingCallback](../documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Позволяет управлять тем, как загружаются внешние ресурсы. |
| [set_RevisionsView](./set_revisionsview/)(Aspose::Words::RevisionsView) | Сеттер для [Aspose::Words::Document::get_RevisionsView](./get_revisionsview/). |
| [set_ShadeFormData](./set_shadeformdata/)(bool) | Сеттер для [Aspose::Words::Document::get_ShadeFormData](./get_shadeformdata/). |
| [set_ShowGrammaticalErrors](./set_showgrammaticalerrors/)(bool) | Сеттер для [Aspose::Words::Document::get_ShowGrammaticalErrors](./get_showgrammaticalerrors/). |
| [set_ShowSpellingErrors](./set_showspellingerrors/)(bool) | Сеттер для [Aspose::Words::Document::get_ShowSpellingErrors](./get_showspellingerrors/). |
| [set_SpellingChecked](./set_spellingchecked/)(bool) | Сеттер для [Aspose::Words::Document::get_SpellingChecked](./get_spellingchecked/). |
| [set_TrackRevisions](./set_trackrevisions/)(bool) | Сеттер для [Aspose::Words::Document::get_TrackRevisions](./get_trackrevisions/). |
| [set_VbaProject](./set_vbaproject/)(const System::SharedPtr\<Aspose::Words::Vba::VbaProject\>\&) | Сеттер для [Aspose::Words::Document::get_VbaProject](./get_vbaproject/). |
| [set_WarningCallback](../documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Сеттер для [Aspose::Words::DocumentBase::get_WarningCallback](../documentbase/get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&, System::DateTime) | Автоматически начинает помечать все последующие изменения, которые вы вносите в документ программно, как изменения ревизий. |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&) | Автоматически начинает помечать все последующие изменения, которые вы вносите в документ программно, как изменения ревизий. |
| [StopTrackRevisions](./stoptrackrevisions/)() | Останавливает автоматическое помечание изменений документа как ревизий. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Отвязывает поля во всём документе. |
| [Unprotect](./unprotect/)() | Снимает защиту с документа независимо от пароля. |
| [Unprotect](./unprotect/)(const System::String\&) | Снимает защиту с документа, если указан правильный пароль. |
| [UpdateActualReferenceMarks](./updateactualreferencemarks/)() | Обновляет свойство [ActualReferenceMark](../../aspose.words.notes/footnote/get_actualreferencemark/) всех сносок и концевых сносок в документе. |
| [UpdateFields](./updatefields/)() | Обновляет значения полей во всём документе. |
| [UpdateListLabels](./updatelistlabels/)() | Обновляет метки списков для всех элементов списка в документе. |
| [UpdatePageLayout](./updatepagelayout/)() | Перестраивает разметку страниц документа. |
| [UpdateTableLayout](./updatetablelayout/)() | Реализует более ранний подход к перерасчёту ширины столбцов таблицы, который имеет известные проблемы. |
| [UpdateThumbnail](./updatethumbnail/)(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) | Обновляет [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) документа в соответствии с указанными параметрами. |
| [UpdateThumbnail](./updatethumbnail/)() | Обновляет [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) документа, используя параметры по умолчанию. |
| [UpdateWordCount](./updatewordcount/)() | Обновляет свойства подсчёта слов в документе. |
| [UpdateWordCount](./updatewordcount/)(bool) | Обновляет свойства подсчёта слов в документе, при необходимости обновляет свойство [Lines](../../aspose.words.properties/builtindocumentproperties/get_lines/). |
## Примечания


Объект [Document](./) является центральным объектом в библиотеке Aspose.Words.

Чтобы загрузить существующий документ в любом из форматов [LoadFormat](../loadformat/), передайте имя файла или поток в один из конструкторов [Document](./). Чтобы создать пустой документ, вызовите конструктор без параметров.

Используйте одну из перегрузок метода Save, чтобы сохранить документ в любом из форматов [SaveFormat](../saveformat/).

Чтобы отрисовать страницы документа непосредственно на объект **Graphics**, используйте метод [RenderToScale()](../) или [RenderToSize()](../).

Чтобы распечатать документ, используйте один из методов [Print()](../).

[MailMerge](./get_mailmerge/) is the [Aspose.Words](../)'s reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

[Document](./) stores document-wide information such as [Styles](../documentbase/get_styles/), [BuiltInDocumentProperties](./get_builtindocumentproperties/), [CustomDocumentProperties](./get_customdocumentproperties/), lists and macros. Most of these objects are accessible via the corresponding properties of the [Document](./).

Объект [Document](./) является корневым узлом дерева, которое содержит все остальные узлы документа. Дерево реализует шаблон Composite и во многих отношениях похоже на XmlDocument. Содержимое документа может свободно изменяться программно:

* The nodes of the document can be accessed via typed collections, for example [Sections](./get_sections/), [ParagraphCollection](../paragraphcollection/) etc.
* The nodes of the document can be selected by their node type using [GetChildNodes()](../compositenode/getchildnodes/) or using an XPath query with [SelectNodes()](../) or [SelectSingleNode()](../).
* Content nodes can be added or removed from anywhere in the document using [InsertBefore1()</see>, <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../), [RemoveChild``1()](../) and other methods provided by the base class [CompositeNode](../compositenode/).
* The formatting attributes of each node can be changed via the properties of that node.



Рассмотрите возможность использования [DocumentBuilder](../documentbuilder/), который упрощает задачу программного создания или заполнения дерева документа.

Объект [Document](./) может содержать только объекты [Section](../section/).

В Microsoft Word корректный документ должен содержать как минимум один раздел.
## См. также

* Class [DocumentBase](../documentbase/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
