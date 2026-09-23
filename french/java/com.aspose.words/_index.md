---
title: "com.aspose.words"
linktitle: "com.aspose.words"
second_title: "Aspose.Words pour Java"
description: "Le package com.aspose.words fournit des classes pour générer, convertir, modifier, rendre et imprimer des documents Microsoft Word sans utiliser Microsoft Word en Java."
type: docs
weight: 10
url: /fr/java/com.aspose.words/
---


Le package **com.aspose.words** fournit des classes pour générer, convertir, modifier, rendre et imprimer des documents Microsoft Word sans utiliser Microsoft Word.

Aspose.Words est entièrement écrit en Java. Microsoft Word n'est pas requis pour utiliser Aspose.Words.

Les classes du package **com.aspose.words** empruntent les meilleures pratiques de deux frameworks bien connus : Microsoft Word Automation et System.Xml. Un document dans Aspose.Words est représenté par un arbre de nœuds, similaire au DOM XML. Dans la mesure du possible, les noms de classes, de méthodes et de propriétés correspondent à ceux trouvés dans Microsoft Word Automation.

Les principales classes de cet espace de noms sont :

 *  **Document** is the main class of the object model that represents a Microsoft Word document.
 *  **DocumentBuilder** provides an easy way to insert content and formatting into a document.
 *  **Node** is the base class for all nodes in the document.
 *  **CompositeNode** is the base class for all nodes of the document that can contain other nodes, for example **Paragraph**, **Section** and **Table** and .

Le package **com.aspose.words** contient également des classes qui constituent le moteur de génération de rapports d'Aspose.Words. Le moteur de génération de rapports permet de remplir rapidement et facilement des documents conçus dans Microsoft Word avec des données provenant de diverses sources telles que **java.sql.ResultSet**, **array of ResultSets**, **com.aspose.words.net.System.Data.DataSet** ou un **array of values**.

L'objet **MailMerge** qui fournit l'accès aux fonctionnalités de génération de rapports est disponible via la propriété **Document.MailMerge**.


## Classes

| Classe | Description |
| --- | --- |
| [AbsolutePositionTab](../com.aspose.words/absolutepositiontab/) | Un onglet de position absolue est un caractère utilisé pour avancer la position sur la ligne de texte actuelle lors de l'affichage de ce contenu WordprocessingML. |
| [Adjustment](../com.aspose.words/adjustment/) | Représente les valeurs d'ajustement appliquées à la forme spécifiée. |
| [AdjustmentCollection](../com.aspose.words/adjustmentcollection/) | Représente une collection en lecture seule de valeurs d'ajustement [Adjustment](../com.aspose.words/adjustment/) appliquées à la forme spécifiée. |
| [AdvancedCompareOptions](../com.aspose.words/advancedcompareoptions/) | Permet de définir des options de comparaison avancées. |
| [AiModel](../com.aspose.words/aimodel/) | Une classe abstraite représentant l'intégration avec divers modèles d'IA au sein d'Aspose.Words. |
| [AiModelType](../com.aspose.words/aimodeltype/) | Représente les types de [AiModel](../com.aspose.words/aimodel/) qui peuvent être intégrés dans le flux de traitement des documents. |
| [AnthropicAiModel](../com.aspose.words/anthropicaimodel/) | Une classe abstraite représentant l'intégration avec les modèles d'IA d'Anthropic au sein d'Aspose.Words. |
| [ArrowLength](../com.aspose.words/arrowlength/) | Longueur de la flèche à l'extrémité d'une ligne. |
| [ArrowType](../com.aspose.words/arrowtype/) | Spécifie le type d'une flèche à l'extrémité d'une ligne. |
| [ArrowWidth](../com.aspose.words/arrowwidth/) | Largeur de la flèche à l'extrémité d'une ligne. |
| [AsposeWordsPrintDocument](../com.aspose.words/asposewordsprintdocument/) | Fournit une implémentation par défaut pour l'impression d'un [Document](../com.aspose.words/document/) dans le cadre d'impression Java. |
| [AutoFitBehavior](../com.aspose.words/autofitbehavior/) | Détermine comment Aspose.Words redimensionne le tableau lorsque vous invoquez la méthode **M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**. |
| [AxisBound](../com.aspose.words/axisbound/) | Représente la borne minimale ou maximale des valeurs d'axe. |
| [AxisBuiltInUnit](../com.aspose.words/axisbuiltinunit/) | Spécifie les unités d'affichage pour un axe. |
| [AxisCategoryType](../com.aspose.words/axiscategorytype/) | Spécifie le type d'un axe de catégorie. |
| [AxisCrosses](../com.aspose.words/axiscrosses/) | Spécifie les points de croisement possibles pour un axe. |
| [AxisDisplayUnit](../com.aspose.words/axisdisplayunit/) | Fournit l'accès aux options de mise à l'échelle des unités d'affichage pour l'axe des valeurs. |
| [AxisGroup](../com.aspose.words/axisgroup/) | Représente un type de groupe d'axes de graphique. |
| [AxisScaleType](../com.aspose.words/axisscaletype/) | Spécifie les types d'échelle possibles pour un axe. |
| [AxisScaling](../com.aspose.words/axisscaling/) | Représente les options de mise à l'échelle de l'axe. |
| [AxisTickLabelPosition](../com.aspose.words/axisticklabelposition/) | Spécifie les positions possibles pour les étiquettes de graduation. |
| [AxisTickLabels](../com.aspose.words/axisticklabels/) | Représente les propriétés des étiquettes de marques de graduation de l'axe. |
| [AxisTickMark](../com.aspose.words/axistickmark/) | Spécifie les positions possibles pour les marques de graduation. |
| [AxisTimeUnit](../com.aspose.words/axistimeunit/) | Spécifie l'unité de temps pour les axes. |
| [BarcodeParameters](../com.aspose.words/barcodeparameters/) | Classe conteneur pour les paramètres de code-barres à transmettre à BarcodeGenerator. |
| [BaseWebExtensionCollection](../com.aspose.words/basewebextensioncollection/) | Classe de base pour les collections [TaskPaneCollection](../com.aspose.words/taskpanecollection/), [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection/), [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection/) et [WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection/). |
| [BaselineAlignment](../com.aspose.words/baselinealignment/) | Spécifie la position verticale des polices sur une ligne. |
| [BasicTextShaperCache](../com.aspose.words/basictextshapercache/) | Implémente un cache de base pour les instances de [ITextShaper](../com.aspose.words/itextshaper/). |
| [Bibliography](../com.aspose.words/bibliography/) | Représente la liste des sources bibliographiques disponibles dans le document. |
| [BlockImportMode](../com.aspose.words/blockimportmode/) | Spécifie comment les propriétés des éléments de niveau bloc sont importées depuis des documents basés sur HTML. |
| [Body](../com.aspose.words/body/) | Représente un conteneur pour le texte principal d'une section. |
| [Bookmark](../com.aspose.words/bookmark/) | Représente un seul signet. |
| [BookmarkCollection](../com.aspose.words/bookmarkcollection/) | Une collection d'objets [Bookmark](../com.aspose.words/bookmark/) qui représentent les signets dans la plage spécifiée. |
| [BookmarkEnd](../com.aspose.words/bookmarkend/) | Représente la fin d'un signet dans un document Word. |
| [BookmarkStart](../com.aspose.words/bookmarkstart/) | Représente le début d'un signet dans un document Word. |
| [BookmarksOutlineLevelCollection](../com.aspose.words/bookmarksoutlinelevelcollection/) | Une collection de niveaux de plan de signets individuels. |
| [Border](../com.aspose.words/border/) | Représente une bordure d'un objet. |
| [BorderCollection](../com.aspose.words/bordercollection/) | Une collection d'objets [Border](../com.aspose.words/border/). |
| [BorderType](../com.aspose.words/bordertype/) | Spécifie les côtés d'une bordure. |
| [BreakType](../com.aspose.words/breaktype/) | Spécifie le type de saut à l'intérieur d'un document. |
| [BubbleSizeCollection](../com.aspose.words/bubblesizecollection/) | Représente une collection de tailles de bulles pour une série de graphique. |
| [BuildVersionInfo](../com.aspose.words/buildversioninfo/) | Fournit des informations sur le nom et la version du produit actuel. |
| [BuildingBlock](../com.aspose.words/buildingblock/) | Représente une entrée de glossaire de document telle qu'un Building Block, un AutoText ou une entrée AutoCorrect. |
| [BuildingBlockBehavior](../com.aspose.words/buildingblockbehavior/) | Spécifie le comportement qui doit être appliqué au contenu du building block lorsqu'il est inséré dans le document principal. |
| [BuildingBlockCollection](../com.aspose.words/buildingblockcollection/) | Une collection d'objets [BuildingBlock](../com.aspose.words/buildingblock/) dans le document. |
| [BuildingBlockGallery](../com.aspose.words/buildingblockgallery/) | Spécifie la galerie prédéfinie dans laquelle un building block est classé. |
| [BuildingBlockType](../com.aspose.words/buildingblocktype/) | Spécifie un type de building block. |
| [BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties/) | Une collection de propriétés de document intégrées. |
| [CalendarType](../com.aspose.words/calendartype/) | Spécifie le type d'un calendrier. |
| [Cell](../com.aspose.words/cell/) | Représente une cellule de tableau. |
| [CellCollection](../com.aspose.words/cellcollection/) | Fournit un accès typé à une collection de nœuds [Cell](../com.aspose.words/cell/). |
| [CellFormat](../com.aspose.words/cellformat/) | Représente toute la mise en forme d'une cellule de tableau. |
| [CellMerge](../com.aspose.words/cellmerge/) | Spécifie comment une cellule d'un tableau est fusionnée avec d'autres cellules. |
| [CellVerticalAlignment](../com.aspose.words/cellverticalalignment/) | Spécifie la justification verticale du texte à l'intérieur d'une cellule de tableau. |
| [CertificateHolder](../com.aspose.words/certificateholder/) | Représente un conteneur d'instance **X509Certificate2**. |
| [ChapterPageSeparator](../com.aspose.words/chapterpageseparator/) | Définit le caractère séparateur qui apparaît entre le chapitre et le numéro de page. |
| [Chart](../com.aspose.words/chart/) | Fournit l'accès aux propriétés de forme du graphique. |
| [ChartAxis](../com.aspose.words/chartaxis/) | Représente les options d'axe du graphique. |
| [ChartAxisCollection](../com.aspose.words/chartaxiscollection/) | Représente une collection d'axes de graphique. |
| [ChartAxisTitle](../com.aspose.words/chartaxistitle/) | Fournit l'accès aux propriétés du titre de l'axe. |
| [ChartAxisType](../com.aspose.words/chartaxistype/) | Spécifie le type d'axe du graphique. |
| [ChartDataLabel](../com.aspose.words/chartdatalabel/) | Représente l'étiquette de données sur un point de graphique ou une ligne de tendance. |
| [ChartDataLabelCollection](../com.aspose.words/chartdatalabelcollection/) | Représente une collection de [ChartDataLabel](../com.aspose.words/chartdatalabel/). |
| [ChartDataLabelLocationMode](../com.aspose.words/chartdatalabellocationmode/) | Spécifie comment les valeurs \\u200b\\u200bqui spécifient l'emplacement d'une étiquette de données - les propriétés [ChartDataLabel.#getLeft()](../com.aspose.words/chartdatalabel/#getLeft) / [ChartDataLabel.#setLeft(double)](../com.aspose.words/chartdatalabel/#setLeft-double) et [ChartDataLabel.#getTop()](../com.aspose.words/chartdatalabel/#getTop) / [ChartDataLabel.#setTop(double)](../com.aspose.words/chartdatalabel/#setTop-double) - sont interprétées. |
| [ChartDataLabelPosition](../com.aspose.words/chartdatalabelposition/) | Spécifie la position d'une étiquette de données du graphique. |
| [ChartDataPoint](../com.aspose.words/chartdatapoint/) | Permet de spécifier le formatage d'un seul point de données sur le graphique. |
| [ChartDataPointCollection](../com.aspose.words/chartdatapointcollection/) | Représente une collection de [ChartDataPoint](../com.aspose.words/chartdatapoint/). |
| [ChartDataTable](../com.aspose.words/chartdatatable/) | Permet de spécifier les propriétés d'un tableau de données du graphique. |
| [ChartFormat](../com.aspose.words/chartformat/) | Représente le formatage d'un élément de graphique. |
| [ChartLegend](../com.aspose.words/chartlegend/) | Représente les propriétés de la légende du graphique. |
| [ChartLegendEntry](../com.aspose.words/chartlegendentry/) | Représente une entrée de légende de graphique. |
| [ChartLegendEntryCollection](../com.aspose.words/chartlegendentrycollection/) | Représente une collection d'entrées de légende de graphique. |
| [ChartMarker](../com.aspose.words/chartmarker/) | Représente un marqueur de données de graphique. |
| [ChartMultilevelValue](../com.aspose.words/chartmultilevelvalue/) | Représente une valeur pour les graphiques affichant des données à plusieurs niveaux. |
| [ChartNumberFormat](../com.aspose.words/chartnumberformat/) | Représente le format numérique de l'élément parent. |
| [ChartSeries](../com.aspose.words/chartseries/) | Représente les propriétés de séries de graphique. |
| [ChartSeriesCollection](../com.aspose.words/chartseriescollection/) | Représente une collection de [ChartSeries](../com.aspose.words/chartseries/). |
| [ChartSeriesGroup](../com.aspose.words/chartseriesgroup/) | Représente les propriétés d'un groupe de séries de graphique, c'est‑à‑dire les propriétés des séries de graphique du même type associées aux mêmes axes. |
| [ChartSeriesGroupCollection](../com.aspose.words/chartseriesgroupcollection/) | Représente une collection d'objets [ChartSeriesGroup](../com.aspose.words/chartseriesgroup/). |
| [ChartSeriesType](../com.aspose.words/chartseriestype/) | Spécifie un type de série de graphique. |
| [ChartShapeType](../com.aspose.words/chartshapetype/) | Spécifie le type de forme des éléments de graphique. |
| [ChartStyle](../com.aspose.words/chartstyle/) | Spécifie les styles prédéfinis d'un graphique. |
| [ChartTitle](../com.aspose.words/charttitle/) | Fournit l'accès aux propriétés du titre du graphique. |
| [ChartType](../com.aspose.words/charttype/) | Spécifie le type d'un graphique. |
| [ChartXValue](../com.aspose.words/chartxvalue/) | Représente une valeur X pour une série de graphique. |
| [ChartXValueCollection](../com.aspose.words/chartxvaluecollection/) | Représente une collection de valeurs X pour une série de graphique. |
| [ChartXValueType](../com.aspose.words/chartxvaluetype/) | Permet de spécifier le type d'une valeur X d'une série de graphique. |
| [ChartYValue](../com.aspose.words/chartyvalue/) | Représente une valeur Y pour une série de graphique. |
| [ChartYValueCollection](../com.aspose.words/chartyvaluecollection/) | Représente une collection de valeurs Y pour une série de graphique. |
| [ChartYValueType](../com.aspose.words/chartyvaluetype/) | Permet de spécifier le type d'une valeur Y d'une série de graphique. |
| [CheckBoxControl](../com.aspose.words/checkboxcontrol/) | Le contrôle CheckBox bascule une valeur. |
| [CheckGrammarOptions](../com.aspose.words/checkgrammaroptions/) | Permet de spécifier diverses options lors de la vérification grammaticale d'un document à l'aide de l'IA. |
| [ChmLoadOptions](../com.aspose.words/chmloadoptions/) | Permet de spécifier des options supplémentaires lors du chargement d'un document CHM dans un objet [Document](../com.aspose.words/document/). |
| [CleanupOptions](../com.aspose.words/cleanupoptions/) | Permet de spécifier des options pour le nettoyage de documents. |
| [Cluster](../com.aspose.words/cluster/) | Encapsule les points de code et les glyphes composant un graphème. |
| [ColorMode](../com.aspose.words/colormode/) | Spécifie comment les couleurs sont rendues. |
| [ColorPrintMode](../com.aspose.words/colorprintmode/) | Spécifie comment les pages non colorées sont imprimées si l'appareil prend en charge l'impression couleur. |
| [CommandButtonControl](../com.aspose.words/commandbuttoncontrol/) | Le contrôle CommandButton exécute une macro qui effectue une action lorsqu'un utilisateur clique dessus. |
| [Comment](../com.aspose.words/comment/) | Représente un conteneur pour le texte d'un commentaire. |
| [CommentCollection](../com.aspose.words/commentcollection/) | Fournit un accès typé à une collection de nœuds [Comment](../com.aspose.words/comment/). |
| [CommentDisplayMode](../com.aspose.words/commentdisplaymode/) | Spécifie le mode de rendu pour les commentaires de document. |
| [CommentRangeEnd](../com.aspose.words/commentrangeend/) | Indique la fin d'une région de texte associée à un commentaire. |
| [CommentRangeStart](../com.aspose.words/commentrangestart/) | Indique le début d'une région de texte associée à un commentaire. |
| [CompareOptions](../com.aspose.words/compareoptions/) | Permet de choisir des options supplémentaires pour l'opération de comparaison de documents. |
| [Comparer](../com.aspose.words/comparer/) | Fournit des méthodes destinées à comparer des documents. |
| [ComparerContext](../com.aspose.words/comparercontext/) | Contexte du comparateur de documents |
| [ComparisonEvaluationResult](../com.aspose.words/comparisonevaluationresult/) | Le résultat de l'évaluation de la comparaison. |
| [ComparisonExpression](../com.aspose.words/comparisonexpression/) | L'expression de comparaison. |
| [ComparisonTargetType](../com.aspose.words/comparisontargettype/) | Permet de spécifier le document de base qui sera utilisé lors de la comparaison. |
| [Compatibility](../com.aspose.words/compatibility/) | Spécifie les noms des options de compatibilité. |
| [CompatibilityOptions](../com.aspose.words/compatibilityoptions/) | Contient les options de compatibilité (c'est‑à‑dire les préférences utilisateur saisies dans l'onglet **Compatibility** de la boîte de dialogue **Options** de Microsoft Word). |
| [CompositeNode](../com.aspose.words/compositenode/) | Classe de base pour les nœuds pouvant contenir d'autres nœuds. |
| [CompressionLevel](../com.aspose.words/compressionlevel/) | Niveau de compression pour les fichiers OOXML et XPS. |
| [ConditionalStyle](../com.aspose.words/conditionalstyle/) | Représente le formatage spécial appliqué à une zone d'un tableau avec un style de tableau attribué. |
| [ConditionalStyleCollection](../com.aspose.words/conditionalstylecollection/) | Représente une collection d'objets [ConditionalStyle](../com.aspose.words/conditionalstyle/). |
| [ConditionalStyleType](../com.aspose.words/conditionalstyletype/) | Représente les zones de tableau possibles auxquelles un formatage conditionnel peut être défini dans un style de tableau. |
| [ContentDisposition](../com.aspose.words/contentdisposition/) | Énumère les différentes manières de présenter le document dans le navigateur client. |
| [ContinuousSectionRestart](../com.aspose.words/continuoussectionrestart/) | Représente les différents comportements lors du calcul des numéros de page dans une section continue qui redémarre la numérotation des pages. |
| [Contributor](../com.aspose.words/contributor/) | Représente un contributeur de source bibliographique. |
| [ContributorCollection](../com.aspose.words/contributorcollection/) | Représente les contributeurs de sources bibliographiques. |
| [ControlChar](../com.aspose.words/controlchar/) | Caractères de contrôle souvent rencontrés dans les documents. |
| [ConvertUtil](../com.aspose.words/convertutil/) | Fournit des fonctions d'aide pour convertir entre différentes unités de mesure. |
| [Converter](../com.aspose.words/converter/) | Représente un groupe de méthodes destinées à convertir une variété de types de documents différents en une seule ligne de code. |
| [ConverterContext](../com.aspose.words/convertercontext/) | Contexte du convertisseur de documents |
| [Corporate](../com.aspose.words/corporate/) | Représente un contributeur de source bibliographique d'entreprise (une organisation). |
| [CssSavingArgs](../com.aspose.words/csssavingargs/) | Fournit des données pour l'événement [ICssSavingCallback.\#cssSaving(com.aspose.words.CssSavingArgs)](../com.aspose.words/icsssavingcallback/\#cssSaving-com.aspose.words.CssSavingArgs). |
| [CssStyleSheetType](../com.aspose.words/cssstylesheettype/) | Spécifie comment les styles CSS (Cascading Style Sheet) sont exportés vers HTML. |
| [CsvDataLoadOptions](../com.aspose.words/csvdataloadoptions/) | Représente les options d'analyse des données CSV. |
| [CsvDataSource](../com.aspose.words/csvdatasource/) | Fournit l'accès aux données d'un fichier CSV ou d'un flux à utiliser dans un rapport. |
| [CurrentThreadSettings](../com.aspose.words/currentthreadsettings/) | Cette classe aide à définir la locale et le fuseau horaire isolés par thread pour une application Aspose.Words. |
| [CustomDocumentProperties](../com.aspose.words/customdocumentproperties/) | Une collection de propriétés de document personnalisées. |
| [CustomPart](../com.aspose.words/custompart/) | Représente une partie personnalisée (contenu arbitraire) qui n'est pas définie par la norme ISO/IEC 29500. |
| [CustomPartCollection](../com.aspose.words/custompartcollection/) | Représente une collection d'objets [CustomPart](../com.aspose.words/custompart/). |
| [CustomXmlPart](../com.aspose.words/customxmlpart/) | Représente une partie de stockage de données XML personnalisée (données XML personnalisées au sein d'un package). |
| [CustomXmlPartCollection](../com.aspose.words/customxmlpartcollection/) | Représente une collection de parties XML personnalisées. |
| [CustomXmlProperty](../com.aspose.words/customxmlproperty/) | Représente un attribut XML personnalisé unique ou une propriété de balise intelligente. |
| [CustomXmlPropertyCollection](../com.aspose.words/customxmlpropertycollection/) | Représente une collection d'attributs XML personnalisés ou de propriétés de balises intelligentes. |
| [CustomXmlSchemaCollection](../com.aspose.words/customxmlschemacollection/) | Une collection de chaînes qui représentent les schémas XML associés à une partie XML personnalisée. |
| [DashStyle](../com.aspose.words/dashstyle/) | Style de ligne pointillée. |
| [DefaultFontSubstitutionRule](../com.aspose.words/defaultfontsubstitutionrule/) | Règle de substitution de police par défaut. |
| [DigitalSignature](../com.aspose.words/digitalsignature/) | Représente une signature numérique sur un document et le résultat de sa vérification. |
| [DigitalSignatureCollection](../com.aspose.words/digitalsignaturecollection/) | Fournit une collection en lecture seule de signatures numériques attachées à un document. |
| [DigitalSignatureDetails](../com.aspose.words/digitalsignaturedetails/) | Contient les détails pour signer un document avec une signature numérique. |
| [DigitalSignatureType](../com.aspose.words/digitalsignaturetype/) | Spécifie le type d'une signature numérique. |
| [DigitalSignatureUtil](../com.aspose.words/digitalsignatureutil/) | Fournit des méthodes pour signer le document. |
| [Direction](../com.aspose.words/direction/) | Direction du texte. |
| [Dml3DEffectsRenderingMode](../com.aspose.words/dml3deffectsrenderingmode/) | Spécifie comment les effets des formes 3D sont rendus. |
| [DmlEffectsRenderingMode](../com.aspose.words/dmleffectsrenderingmode/) | Spécifie comment les effets DrawingML sont rendus vers des formats de page fixes. |
| [DmlRenderingMode](../com.aspose.words/dmlrenderingmode/) | Spécifie comment les formes DrawingML sont rendues vers des formats de page fixes. |
| [DocSaveOptions](../com.aspose.words/docsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#DOC](../com.aspose.words/saveformat/\#DOC) ou [SaveFormat.\#DOT](../com.aspose.words/saveformat/\#DOT). |
| [DoclingSaveOptions](../com.aspose.words/doclingsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#DOCLING](../com.aspose.words/saveformat/\#DOCLING). |
| [Document](../com.aspose.words/document/) | Représente un document Word. |
| [DocumentBase](../com.aspose.words/documentbase/) | Fournit la classe de base abstraite pour le document principal et le document de glossaire d'un document Word. |
| [DocumentBuilder](../com.aspose.words/documentbuilder/) | Fournit des méthodes pour insérer du texte, des images et d'autres contenus, spécifier la police, le formatage des paragraphes et des sections. |
| [DocumentBuilderOptions](../com.aspose.words/documentbuilderoptions/) | Permet de spécifier des options supplémentaires pour le processus de création du document. |
| [DocumentDirection](../com.aspose.words/documentdirection/) | Permet de spécifier la direction du flux de texte dans un document. |
| [DocumentLoadingArgs](../com.aspose.words/documentloadingargs/) | Un argument passé à [IDocumentLoadingCallback.\#notify(com.aspose.words.DocumentLoadingArgs)](../com.aspose.words/idocumentloadingcallback/\#notify-com.aspose.words.DocumentLoadingArgs). |
| [DocumentPartSavingArgs](../com.aspose.words/documentpartsavingargs/) | Fournit des données pour le rappel [IDocumentPartSavingCallback.\#documentPartSaving(com.aspose.words.DocumentPartSavingArgs)](../com.aspose.words/idocumentpartsavingcallback/\#documentPartSaving-com.aspose.words.DocumentPartSavingArgs). |
| [DocumentProperty](../com.aspose.words/documentproperty/) | Représente une propriété de document personnalisée ou intégrée. |
| [DocumentPropertyCollection](../com.aspose.words/documentpropertycollection/) | Classe de base pour les collections [BuiltInDocumentProperties](../com.aspose.words/builtindocumentproperties/) et [CustomDocumentProperties](../com.aspose.words/customdocumentproperties/). |
| [DocumentReaderPluginLoadException](../com.aspose.words/documentreaderpluginloadexception/) | Lancée lors du chargement du document, lorsque le plugin requis pour lire le format du document ne peut pas être chargé. |
| [DocumentRecoveryMode](../com.aspose.words/documentrecoverymode/) | Spécifie les options de récupération disponibles lorsqu'un document rencontre des erreurs lors du chargement. |
| [DocumentSavingArgs](../com.aspose.words/documentsavingargs/) | Un argument passé à [IDocumentSavingCallback.\#notify(com.aspose.words.DocumentSavingArgs)](../com.aspose.words/idocumentsavingcallback/\#notify-com.aspose.words.DocumentSavingArgs). |
| [DocumentSecurity](../com.aspose.words/documentsecurity/) | Utilisé comme valeur pour la propriété [BuiltInDocumentProperties.\#getSecurity()](../com.aspose.words/builtindocumentproperties/\#getSecurity) / [BuiltInDocumentProperties.\#setSecurity(int)](../com.aspose.words/builtindocumentproperties/\#setSecurity-int). |
| [DocumentSplitCriteria](../com.aspose.words/documentsplitcriteria/) | Spécifie comment le document est découpé en parties lors de l'enregistrement au format [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB) ou [SaveFormat.\#AZW\_3](../com.aspose.words/saveformat/\#AZW-3). |
| [DocumentVisitor](../com.aspose.words/documentvisitor/) | Classe de base pour les visiteurs de documents personnalisés. |
| [DownsampleOptions](../com.aspose.words/downsampleoptions/) | Permet de spécifier les options de sous-échantillonnage. |
| [DropCapPosition](../com.aspose.words/dropcapposition/) | Spécifie la position du texte en lettrine. |
| [DropDownItemCollection](../com.aspose.words/dropdownitemcollection/) | Une collection de chaînes représentant tous les éléments d'un champ de formulaire déroulant. |
| [EditableRange](../com.aspose.words/editablerange/) | Représente une plage modifiable unique. |
| [EditableRangeEnd](../com.aspose.words/editablerangeend/) | Représente la fin d'une plage modifiable dans un document Word. |
| [EditableRangeStart](../com.aspose.words/editablerangestart/) | Représente le début d'une plage modifiable dans un document Word. |
| [EditingLanguage](../com.aspose.words/editinglanguage/) | Spécifie la langue d'édition. |
| [EditorType](../com.aspose.words/editortype/) | Spécifie l'ensemble des alias possibles (ou groupes d'édition) pouvant être utilisés comme alias pour déterminer si l'utilisateur actuel est autorisé à modifier une plage unique définie par une plage modifiable dans un document. |
| [EmbeddedFontFormat](../com.aspose.words/embeddedfontformat/) | Spécifie le format d'une police incorporée particulière à l'intérieur de l'objet [FontInfo](../com.aspose.words/fontinfo/). |
| [EmbeddedFontStyle](../com.aspose.words/embeddedfontstyle/) | Spécifie le style d'une police incorporée à l'intérieur d'un objet [FontInfo](../com.aspose.words/fontinfo/). |
| [EmfPlusDualRenderingMode](../com.aspose.words/emfplusdualrenderingmode/) | Spécifie comment Aspose.Words doit rendre les métafichiers EMF+ Dual. |
| [EmphasisMark](../com.aspose.words/emphasismark/) | Spécifie les types possibles de marque d'emphase. |
| [EndCap](../com.aspose.words/endcap/) | Spécifie le style de terminaison de ligne. |
| [EndnoteOptions](../com.aspose.words/endnoteoptions/) | Représente les options de numérotation des notes de fin pour un document ou une section. |
| [EndnotePosition](../com.aspose.words/endnoteposition/) | Définit la position de la note de fin. |
| [ExportFontFormat](../com.aspose.words/exportfontformat/) | Indique le format utilisé pour exporter les polices lors du rendu au format HTML fixe. |
| [ExportHeadersFootersMode](../com.aspose.words/exportheadersfootersmode/) | Spécifie comment les en-têtes et pieds de page sont exportés vers HTML, MHTML ou EPUB. |
| [ExportListLabels](../com.aspose.words/exportlistlabels/) | Spécifie comment les libellés de listes sont exportés vers HTML, MHTML et EPUB. |
| [Field](../com.aspose.words/field/) | Représente un champ de document Microsoft Word. |
| [FieldAddIn](../com.aspose.words/fieldaddin/) | Implémente le champ ADDIN. |
| [FieldAddressBlock](../com.aspose.words/fieldaddressblock/) | Implémente le champ ADDRESSBLOCK. |
| [FieldAdvance](../com.aspose.words/fieldadvance/) | Implémente le champ ADVANCE. |
| [FieldArgumentBuilder](../com.aspose.words/fieldargumentbuilder/) | Construit un argument de champ complexe composé de champs, de nœuds et de texte brut. |
| [FieldAsk](../com.aspose.words/fieldask/) | Implémente le champ ASK. |
| [FieldAuthor](../com.aspose.words/fieldauthor/) | Implémente le champ AUTHOR. |
| [FieldAutoNum](../com.aspose.words/fieldautonum/) | Implémente le champ AUTONUM. |
| [FieldAutoNumLgl](../com.aspose.words/fieldautonumlgl/) | Implémente le champ AUTONUMLGL. |
| [FieldAutoNumOut](../com.aspose.words/fieldautonumout/) | Implémente le champ AUTONUMOUT. |
| [FieldAutoText](../com.aspose.words/fieldautotext/) | Implémente le champ AUTOTEXT. |
| [FieldAutoTextList](../com.aspose.words/fieldautotextlist/) | Implémente le champ AUTOTEXTLIST. |
| [FieldBarcode](../com.aspose.words/fieldbarcode/) | Implémente le champ BARCODE. |
| [FieldBibliography](../com.aspose.words/fieldbibliography/) | Implémente le champ BIBLIOGRAPHY. |
| [FieldBidiOutline](../com.aspose.words/fieldbidioutline/) | Implémente le champ BIDIOUTLINE. |
| [FieldBuilder](../com.aspose.words/fieldbuilder/) | Construit un champ à partir de jetons de code de champ (arguments et commutateurs). |
| [FieldChar](../com.aspose.words/fieldchar/) | Classe de base pour les nœuds qui représentent les caractères de champ dans un document. |
| [FieldCitation](../com.aspose.words/fieldcitation/) | Implémente le champ CITATION. |
| [FieldCollection](../com.aspose.words/fieldcollection/) | Une collection d'objets [Field](../com.aspose.words/field/) qui représente les champs dans la plage spécifiée. |
| [FieldComments](../com.aspose.words/fieldcomments/) | Implémente le champ COMMENTS. |
| [FieldCompare](../com.aspose.words/fieldcompare/) | Implémente le champ COMPARE. |
| [FieldCreateDate](../com.aspose.words/fieldcreatedate/) | Implémente le champ CREATEDATE. |
| [FieldData](../com.aspose.words/fielddata/) | Implémente le champ DATA. |
| [FieldDatabase](../com.aspose.words/fielddatabase/) | Implémente le champ DATABASE. |
| [FieldDatabaseDataRow](../com.aspose.words/fielddatabasedatarow/) | Fournit des données pour le résultat du champ [FieldDatabase](../com.aspose.words/fielddatabase/). |
| [FieldDatabaseDataTable](../com.aspose.words/fielddatabasedatatable/) | Fournit des données pour le résultat du champ [FieldDatabase](../com.aspose.words/fielddatabase/). |
| [FieldDate](../com.aspose.words/fielddate/) | Implémente le champ DATE. |
| [FieldDde](../com.aspose.words/fielddde/) | Implémente le champ DDE. |
| [FieldDdeAuto](../com.aspose.words/fieldddeauto/) | Implémente le champ DDEAUTO. |
| [FieldDisplayBarcode](../com.aspose.words/fielddisplaybarcode/) | Implémente le champ DISPLAYBARCODE. |
| [FieldDocProperty](../com.aspose.words/fielddocproperty/) | Implémente le champ DOCPROPERTY. |
| [FieldDocVariable](../com.aspose.words/fielddocvariable/) | Implémente le champ DOCVARIABLE. |
| [FieldEQ](../com.aspose.words/fieldeq/) | Implémente le champ EQ. |
| [FieldEditTime](../com.aspose.words/fieldedittime/) | Implémente le champ EDITTIME. |
| [FieldEmbed](../com.aspose.words/fieldembed/) | Implémente le champ EMBED. |
| [FieldEnd](../com.aspose.words/fieldend/) | Représente la fin d'un champ Word dans un document. |
| [FieldFileName](../com.aspose.words/fieldfilename/) | Implémente le champ FILENAME. |
| [FieldFileSize](../com.aspose.words/fieldfilesize/) | Implémente le champ FILESIZE. |
| [FieldFillIn](../com.aspose.words/fieldfillin/) | Implémente le champ FILLIN. |
| [FieldFootnoteRef](../com.aspose.words/fieldfootnoteref/) | Implémente le champ FOOTNOTEREF. |
| [FieldFormCheckBox](../com.aspose.words/fieldformcheckbox/) | Implémente le champ FORMCHECKBOX. |
| [FieldFormDropDown](../com.aspose.words/fieldformdropdown/) | Implémente le champ FORMDROPDOWN. |
| [FieldFormText](../com.aspose.words/fieldformtext/) | Implémente le champ FORMTEXT. |
| [FieldFormat](../com.aspose.words/fieldformat/) | Fournit un accès typé aux formats numériques, de date et d'heure du champ, ainsi qu'au formatage général. |
| [FieldFormula](../com.aspose.words/fieldformula/) | Implémente le champ = (formule). |
| [FieldGlossary](../com.aspose.words/fieldglossary/) | Implémente le champ GLOSSARY. |
| [FieldGoToButton](../com.aspose.words/fieldgotobutton/) | Implémente le champ GOTOBUTTON. |
| [FieldGreetingLine](../com.aspose.words/fieldgreetingline/) | Implémente le champ GREETINGLINE. |
| [FieldHyperlink](../com.aspose.words/fieldhyperlink/) | Implémente le champ HYPERLINK |
| [FieldIf](../com.aspose.words/fieldif/) | Implémente le champ IF. |
| [FieldIfComparisonResult](../com.aspose.words/fieldifcomparisonresult/) | Spécifie le résultat de l'évaluation de la condition du champ IF. |
| [FieldImport](../com.aspose.words/fieldimport/) | Implémente le champ IMPORT. |
| [FieldInclude](../com.aspose.words/fieldinclude/) | Implémente le champ INCLUDE. |
| [FieldIncludePicture](../com.aspose.words/fieldincludepicture/) | Implémente le champ INCLUDEPICTURE. |
| [FieldIncludeText](../com.aspose.words/fieldincludetext/) | Implémente le champ INCLUDETEXT. |
| [FieldIndex](../com.aspose.words/fieldindex/) | Implémente le champ INDEX. |
| [FieldIndexFormat](../com.aspose.words/fieldindexformat/) | Spécifie le formatage des champs [FieldIndex](../com.aspose.words/fieldindex/) dans un document. |
| [FieldInfo](../com.aspose.words/fieldinfo/) | Implémente le champ INFO. |
| [FieldKeywords](../com.aspose.words/fieldkeywords/) | Implémente le champ KEYWORDS. |
| [FieldLastSavedBy](../com.aspose.words/fieldlastsavedby/) | Implémente le champ LASTSAVEDBY. |
| [FieldLink](../com.aspose.words/fieldlink/) | Implémente le champ LINK. |
| [FieldListNum](../com.aspose.words/fieldlistnum/) | Implémente le champ LISTNUM. |
| [FieldMacroButton](../com.aspose.words/fieldmacrobutton/) | Implémente le champ MACROBUTTON. |
| [FieldMergeBarcode](../com.aspose.words/fieldmergebarcode/) | Implémente le champ MERGEBARCODE. |
| [FieldMergeField](../com.aspose.words/fieldmergefield/) | Implémente le champ MERGEFIELD. |
| [FieldMergeRec](../com.aspose.words/fieldmergerec/) | Implémente le champ MERGEREC. |
| [FieldMergeSeq](../com.aspose.words/fieldmergeseq/) | Implémente le champ MERGESEQ. |
| [FieldMergingArgs](../com.aspose.words/fieldmergingargs/) | Fournit des données pour l'événement **MergeField**. |
| [FieldMergingArgsBase](../com.aspose.words/fieldmergingargsbase/) | Classe de base pour [FieldMergingArgs](../com.aspose.words/fieldmergingargs/) et [ImageFieldMergingArgs](../com.aspose.words/imagefieldmergingargs/). |
| [FieldNext](../com.aspose.words/fieldnext/) | Implémente le champ NEXT. |
| [FieldNextIf](../com.aspose.words/fieldnextif/) | Implémente le champ NEXTIF. |
| [FieldNoteRef](../com.aspose.words/fieldnoteref/) | Implémente le champ NOTEREF. |
| [FieldNumChars](../com.aspose.words/fieldnumchars/) | Implémente le champ NUMCHARS. |
| [FieldNumPages](../com.aspose.words/fieldnumpages/) | Implémente le champ NUMPAGES. |
| [FieldNumWords](../com.aspose.words/fieldnumwords/) | Implémente le champ NUMWORDS. |
| [FieldOcx](../com.aspose.words/fieldocx/) | Implémente le champ OCX. |
| [FieldOptions](../com.aspose.words/fieldoptions/) | Représente les options pour contrôler la gestion des champs dans un document. |
| [FieldPage](../com.aspose.words/fieldpage/) | Implémente le champ PAGE. |
| [FieldPageRef](../com.aspose.words/fieldpageref/) | Implémente le champ PAGEREF. |
| [FieldPrint](../com.aspose.words/fieldprint/) | Implémente le champ PRINT. |
| [FieldPrintDate](../com.aspose.words/fieldprintdate/) | Implémente le champ PRINTDATE. |
| [FieldPrivate](../com.aspose.words/fieldprivate/) | Implémente le champ PRIVATE. |
| [FieldQuote](../com.aspose.words/fieldquote/) | Implémente le champ QUOTE. |
| [FieldRD](../com.aspose.words/fieldrd/) | Implémente le champ RD. |
| [FieldRef](../com.aspose.words/fieldref/) | Implémente le champ REF. |
| [FieldRevNum](../com.aspose.words/fieldrevnum/) | Implémente le champ REVNUM. |
| [FieldSaveDate](../com.aspose.words/fieldsavedate/) | Implémente le champ SAVEDATE. |
| [FieldSection](../com.aspose.words/fieldsection/) | Implémente le champ SECTION. |
| [FieldSectionPages](../com.aspose.words/fieldsectionpages/) | Implémente le champ SECTIONPAGES. |
| [FieldSeparator](../com.aspose.words/fieldseparator/) | Représente un séparateur de champ Word qui sépare le code du champ du résultat du champ. |
| [FieldSeq](../com.aspose.words/fieldseq/) | Implémente le champ SEQ. |
| [FieldSet](../com.aspose.words/fieldset/) | Implémente le champ SET. |
| [FieldShape](../com.aspose.words/fieldshape/) | Implémente le champ SHAPE. |
| [FieldSkipIf](../com.aspose.words/fieldskipif/) | Implémente le champ SKIPIF. |
| [FieldStart](../com.aspose.words/fieldstart/) | Représente le début d'un champ Word dans un document. |
| [FieldStyleRef](../com.aspose.words/fieldstyleref/) | Implémente le champ STYLEREF. |
| [FieldSubject](../com.aspose.words/fieldsubject/) | Implémente le champ SUBJECT. |
| [FieldSymbol](../com.aspose.words/fieldsymbol/) | Implémente un champ SYMBOL. |
| [FieldTA](../com.aspose.words/fieldta/) | Implémente le champ TA. |
| [FieldTC](../com.aspose.words/fieldtc/) | Implémente le champ TC. |
| [FieldTemplate](../com.aspose.words/fieldtemplate/) | Implémente le champ TEMPLATE. |
| [FieldTime](../com.aspose.words/fieldtime/) | Implémente le champ TIME. |
| [FieldTitle](../com.aspose.words/fieldtitle/) | Implémente le champ TITLE. |
| [FieldToa](../com.aspose.words/fieldtoa/) | Implémente le champ TOA. |
| [FieldToc](../com.aspose.words/fieldtoc/) | Implémente le champ TOC. |
| [FieldType](../com.aspose.words/fieldtype/) | Spécifie les types de champs Microsoft Word. |
| [FieldUnknown](../com.aspose.words/fieldunknown/) | Implémente un champ inconnu ou non reconnu. |
| [FieldUpdateCultureSource](../com.aspose.words/fieldupdateculturesource/) | Indique la culture à utiliser lors de la mise à jour du champ. |
| [FieldUpdatingProgressArgs](../com.aspose.words/fieldupdatingprogressargs/) | Fournit des données pour l'événement de progression de mise à jour du champ. |
| [FieldUserAddress](../com.aspose.words/fielduseraddress/) | Implémente le champ USERADDRESS. |
| [FieldUserInitials](../com.aspose.words/fielduserinitials/) | Implémente le champ USERINITIALS. |
| [FieldUserName](../com.aspose.words/fieldusername/) | Implémente le champ USERNAME. |
| [FieldXE](../com.aspose.words/fieldxe/) | Implémente le champ XE. |
| [FileCorruptedException](../com.aspose.words/filecorruptedexception/) | Lancée lors du chargement du document, lorsque le document semble corrompu et impossible à charger. |
| [FileFontSource](../com.aspose.words/filefontsource/) | Représente le fichier de police TrueType unique stocké dans le système de fichiers. |
| [FileFormatInfo](../com.aspose.words/fileformatinfo/) | Contient les données renvoyées par les méthodes de détection du format de document de [FileFormatUtil](../com.aspose.words/fileformatutil/). |
| [FileFormatUtil](../com.aspose.words/fileformatutil/) | Fournit des méthodes utilitaires pour travailler avec les formats de fichiers, comme la détection du format de fichier ou la conversion des extensions de fichiers vers/depuis les énumérations de formats de fichiers. |
| [Fill](../com.aspose.words/fill/) | Représente le format de remplissage d'un objet. |
| [FillType](../com.aspose.words/filltype/) | Spécifie le type de remplissage pour un objet remplissable. |
| [FindReplaceDirection](../com.aspose.words/findreplacedirection/) | Spécifie la direction pour les opérations de remplacement. |
| [FindReplaceOptions](../com.aspose.words/findreplaceoptions/) | Spécifie les options pour les opérations de recherche/remplacement. |
| [FipsUnapprovedOperationException](../com.aspose.words/fipsunapprovedoperationexception/) | Représente l'exception qui est levée lorsqu'on tente d'utiliser la cryptographie de manière incorrecte. |
| [FixedPageSaveOptions](../com.aspose.words/fixedpagesaveoptions/) | Contient les options communes qui peuvent être spécifiées lors de l'enregistrement d'un document dans des formats de pages fixes (PDF, XPS, images, etc.). |
| [FlipOrientation](../com.aspose.words/fliporientation/) | Valeurs possibles pour l'orientation d'une forme. |
| [FolderFontSource](../com.aspose.words/folderfontsource/) | Représente le dossier qui contient les fichiers de polices TrueType. |
| [Font](../com.aspose.words/font/) | Contient les attributs de police (nom de police, taille de police, couleur, etc.) pour un objet. |
| [FontConfigSubstitutionRule](../com.aspose.words/fontconfigsubstitutionrule/) | Règle de substitution de configuration de police. |
| [FontEmbeddingLicensingRights](../com.aspose.words/fontembeddinglicensingrights/) | Représente les droits de licence d'intégration pour la police. |
| [FontEmbeddingUsagePermissions](../com.aspose.words/fontembeddingusagepermissions/) | Représente les autorisations d'utilisation d'intégration de police. |
| [FontFallbackSettings](../com.aspose.words/fontfallbacksettings/) | Spécifie les paramètres du mécanisme de secours de police. |
| [FontFamily](../com.aspose.words/fontfamily/) | Représente la famille de police. |
| [FontFeature](../com.aspose.words/fontfeature/) | Les fonctionnalités fournissent des informations sur la façon dont les glyphes sont utilisés dans une police pour rendre un script. |
| [FontInfo](../com.aspose.words/fontinfo/) | Spécifie les informations sur une police utilisée dans le document. |
| [FontInfoCollection](../com.aspose.words/fontinfocollection/) | Représente une collection de polices utilisées dans un document. |
| [FontInfoSubstitutionRule](../com.aspose.words/fontinfosubstitutionrule/) | Règle de substitution d'informations de police. |
| [FontNameSubstitutionRule](../com.aspose.words/fontnamesubstitutionrule/) | Règle de substitution de police pour le traitement du nom de police. |
| [FontPitch](../com.aspose.words/fontpitch/) | Représente le pas de police. |
| [FontSavingArgs](../com.aspose.words/fontsavingargs/) | Fournit des données pour l'événement [IFontSavingCallback.\#fontSaving(com.aspose.words.FontSavingArgs)](../com.aspose.words/ifontsavingcallback/\#fontSaving-com.aspose.words.FontSavingArgs). |
| [FontSettings](../com.aspose.words/fontsettings/) | Spécifie les paramètres de police pour un document. |
| [FontSourceBase](../com.aspose.words/fontsourcebase/) | Il s'agit d'une classe de base abstraite pour les classes qui permettent à l'utilisateur de spécifier diverses sources de police. |
| [FontSourceType](../com.aspose.words/fontsourcetype/) | Spécifie le type de source de police. |
| [FontSubstitutionReason](../com.aspose.words/fontsubstitutionreason/) | Spécifie la raison de la substitution de police. |
| [FontSubstitutionRule](../com.aspose.words/fontsubstitutionrule/) | Il s'agit d'une classe de base abstraite pour la règle de substitution de police. |
| [FontSubstitutionSettings](../com.aspose.words/fontsubstitutionsettings/) | Spécifie les paramètres du mécanisme de substitution de police. |
| [FontSubstitutionWarningInfo](../com.aspose.words/fontsubstitutionwarninginfo/) | Contient des informations sur un avertissement de substitution de police émis par Aspose.Words lors du chargement ou de l'enregistrement du document. |
| [Footnote](../com.aspose.words/footnote/) | Représente un conteneur pour le texte d'une note de bas de page ou d'une note de fin. |
| [FootnoteNumberingRule](../com.aspose.words/footnotenumberingrule/) | Détermine quand le numérotage automatique des notes de bas de page ou des notes de fin redémarre. |
| [FootnoteOptions](../com.aspose.words/footnoteoptions/) | Représente les options de numérotation des notes de bas de page pour un document ou une section. |
| [FootnotePosition](../com.aspose.words/footnoteposition/) | Définit la position de la note de bas de page. |
| [FootnoteSeparator](../com.aspose.words/footnoteseparator/) |  |
| [FootnoteSeparatorCollection](../com.aspose.words/footnoteseparatorcollection/) | Fournit un accès typé aux nœuds **T:Aspose.Words.Notes.FootnoteSeparator** d'un document. |
| [FootnoteSeparatorType](../com.aspose.words/footnoteseparatortype/) | Spécifie le type du séparateur de note de bas de page/de note de fin. |
| [FootnoteType](../com.aspose.words/footnotetype/) | Spécifie s'il s'agit d'une note de bas de page ou d'une note de fin. |
| [FormField](../com.aspose.words/formfield/) | Représente un champ de formulaire unique. |
| [FormFieldCollection](../com.aspose.words/formfieldcollection/) | Une collection d'objets [FormField](../com.aspose.words/formfield/) qui représentent tous les champs de formulaire dans une plage. |
| [Forms2OleControl](../com.aspose.words/forms2olecontrol/) | Représente le contrôle OLE Microsoft Forms 2.0. |
| [Forms2OleControlCollection](../com.aspose.words/forms2olecontrolcollection/) | Représente une collection d'objets [Forms2OleControl](../com.aspose.words/forms2olecontrol/). |
| [Forms2OleControlType](../com.aspose.words/forms2olecontroltype/) | Énumère les types de contrôles Forms 2.0. |
| [FrameFormat](../com.aspose.words/frameformat/) | Représente la mise en forme liée aux cadres pour un paragraphe. |
| [Frameset](../com.aspose.words/frameset/) | Représente une page de cadres ou un cadre unique sur une page de cadres. |
| [FramesetCollection](../com.aspose.words/framesetcollection/) | Représente une collection d'instances de la classe [Frameset](../com.aspose.words/frameset/). |
| [GeneralFormat](../com.aspose.words/generalformat/) | Spécifie un format général appliqué à un résultat numérique, texte ou de tout champ. |
| [GeneralFormatCollection](../com.aspose.words/generalformatcollection/) | Représente une collection typée de formats généraux. |
| [GlossaryDocument](../com.aspose.words/glossarydocument/) | Représente l'élément racine d'un document de glossaire dans un document Word. |
| [GlowFormat](../com.aspose.words/glowformat/) | Représente la mise en forme de lueur pour un objet. |
| [Glyph](../com.aspose.words/glyph/) | Représente un glyphe |
| [GlyphFlags](../com.aspose.words/glyphflags/) |  |
| [GoogleAiModel](../com.aspose.words/googleaimodel/) | Classe représentant l'intégration des modèles d'IA Google (Gemini) dans Aspose.Words. |
| [GradientStop](../com.aspose.words/gradientstop/) | Représente un arrêt de dégradé. |
| [GradientStopCollection](../com.aspose.words/gradientstopcollection/) | Contient une collection d'objets [GradientStop](../com.aspose.words/gradientstop/). |
| [GradientStyle](../com.aspose.words/gradientstyle/) | Spécifie le style d'un remplissage en dégradé. |
| [GradientVariant](../com.aspose.words/gradientvariant/) | Spécifie la variante d'un remplissage en dégradé. |
| [Granularity](../com.aspose.words/granularity/) | Spécifie la granularité des modifications à suivre lors de la comparaison de deux documents. |
| [GraphicsQualityOptions](../com.aspose.words/graphicsqualityoptions/) | Permet de spécifier des **java.awt.RenderingHints** supplémentaires. |
| [GroupShape](../com.aspose.words/groupshape/) | Représente un groupe de formes dans un document. |
| [HeaderFooter](../com.aspose.words/headerfooter/) | Représente un conteneur pour le texte d’en-tête ou de pied de page d’une section. |
| [HeaderFooterBookmarksExportMode](../com.aspose.words/headerfooterbookmarksexportmode/) | Spécifie comment les signets dans les en-têtes/pieds de page sont exportés. |
| [HeaderFooterCollection](../com.aspose.words/headerfootercollection/) | Fournit un accès typé aux nœuds [HeaderFooter](../com.aspose.words/headerfooter/) d’une [Section](../com.aspose.words/section/). |
| [HeaderFooterType](../com.aspose.words/headerfootertype/) | Identifie le type d’en-tête ou de pied de page trouvé dans un fichier Word. |
| [HeightRule](../com.aspose.words/heightrule/) | Spécifie la règle de détermination de la hauteur d’un objet. |
| [HorizontalAlignment](../com.aspose.words/horizontalalignment/) | Spécifie l’alignement horizontal d’une forme flottante, d’un cadre de texte ou d’un tableau flottant. |
| [HorizontalRuleAlignment](../com.aspose.words/horizontalrulealignment/) | Représente l’alignement pour la règle horizontale spécifiée. |
| [HorizontalRuleFormat](../com.aspose.words/horizontalruleformat/) | Représente le formatage de la règle horizontale. |
| [HtmlControlType](../com.aspose.words/htmlcontroltype/) | Type de nœuds de document qui représentent les éléments  et  importés depuis HTML. |
| [HtmlElementSizeOutputMode](../com.aspose.words/htmlelementsizeoutputmode/) | Spécifie comment Aspose.Words exporte les largeurs et hauteurs des éléments vers HTML, MHTML et EPUB. |
| [HtmlFixedPageHorizontalAlignment](../com.aspose.words/htmlfixedpagehorizontalalignment/) | Spécifie l’alignement horizontal des pages dans le document HTML de sortie. |
| [HtmlFixedSaveOptions](../com.aspose.words/htmlfixedsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l’enregistrement d’un document au format [SaveFormat.\#HTML\_FIXED](../com.aspose.words/saveformat/\#HTML-FIXED). |
| [HtmlInsertOptions](../com.aspose.words/htmlinsertoptions/) | Spécifie les options pour la méthode **M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)**. |
| [HtmlLoadOptions](../com.aspose.words/htmlloadoptions/) | Permet de spécifier des options supplémentaires lors du chargement d’un document HTML dans un objet [Document](../com.aspose.words/document/). |
| [HtmlMetafileFormat](../com.aspose.words/htmlmetafileformat/) | Indique le format dans lequel les métafichiers sont enregistrés dans les documents HTML. |
| [HtmlOfficeMathOutputMode](../com.aspose.words/htmlofficemathoutputmode/) | Spécifie comment Aspose.Words exporte OfficeMath vers HTML, MHTML et EPUB. |
| [HtmlSaveOptions](../com.aspose.words/htmlsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l’enregistrement d’un document aux formats [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML), [SaveFormat.\#MHTML](../com.aspose.words/saveformat/\#MHTML), [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB), [SaveFormat.\#AZW\_3](../com.aspose.words/saveformat/\#AZW-3) ou [SaveFormat.\#MOBI](../com.aspose.words/saveformat/\#MOBI). |
| [HtmlVersion](../com.aspose.words/htmlversion/) | Indique la version de HTML utilisée lors de l’enregistrement du document aux formats [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML) et [SaveFormat.\#MHTML](../com.aspose.words/saveformat/\#MHTML). |
| [Hyphenation](../com.aspose.words/hyphenation/) | Fournit des méthodes pour travailler avec les dictionnaires de césure. |
| [HyphenationOptions](../com.aspose.words/hyphenationoptions/) | Permet de configurer les options de césure du document. |
| [ImageBinarizationMethod](../com.aspose.words/imagebinarizationmethod/) | Spécifie la méthode utilisée pour binariser l’image. |
| [ImageColorMode](../com.aspose.words/imagecolormode/) | Spécifie le mode couleur pour les images générées des pages du document. |
| [ImageData](../com.aspose.words/imagedata/) | Définit une image pour une forme. |
| [ImageFieldMergingArgs](../com.aspose.words/imagefieldmergingargs/) | Fournit des données pour l’événement [IFieldMergingCallback.\#imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../com.aspose.words/ifieldmergingcallback/\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs). |
| [ImagePixelFormat](../com.aspose.words/imagepixelformat/) | Spécifie le format de pixel pour les images générées des pages du document. |
| [ImageSaveOptions](../com.aspose.words/imagesaveoptions/) | Permet de spécifier des options supplémentaires lors du rendu des pages de document ou des formes en images. |
| [ImageSavingArgs](../com.aspose.words/imagesavingargs/) | Fournit des données pour l'événement [IImageSavingCallback.#imageSaving(com.aspose.words.ImageSavingArgs)](../com.aspose.words/iimagesavingcallback/#imageSaving-com.aspose.words.ImageSavingArgs). |
| [ImageSize](../com.aspose.words/imagesize/) | Contient des informations sur la taille et la résolution de l'image. |
| [ImageType](../com.aspose.words/imagetype/) | Spécifie le type (format) d'une image dans un document Microsoft Word. |
| [ImageWatermarkOptions](../com.aspose.words/imagewatermarkoptions/) | Contient les options qui peuvent être spécifiées lors de l'ajout d'un filigrane avec une image. |
| [ImlRenderingMode](../com.aspose.words/imlrenderingmode/) | Spécifie comment les objets d'encre (InkML) sont rendus aux formats de page fixe. |
| [ImportFormatMode](../com.aspose.words/importformatmode/) | Spécifie comment le formatage est fusionné lors de l'importation de contenu depuis un autre document. |
| [ImportFormatOptions](../com.aspose.words/importformatoptions/) | Permet de spécifier diverses options d'importation pour formater la sortie. |
| [IncorrectPasswordException](../com.aspose.words/incorrectpasswordexception/) | Lancée si un document est chiffré avec un mot de passe et que le mot de passe spécifié lors de l'ouverture du document est incorrect ou manquant. |
| [Inline](../com.aspose.words/inline/) | Classe de base pour les nœuds de niveau en ligne qui peuvent avoir un formatage de caractères associé, mais ne peuvent pas avoir de nœuds enfants. |
| [InlineStory](../com.aspose.words/inlinestory/) | Classe de base pour les nœuds de niveau en ligne qui peuvent contenir des paragraphes et des tableaux. |
| [InternableComplexAttr](../com.aspose.words/internablecomplexattr/) | Classe de base pour l'attribut complexe internable. |
| [JoinRunsOptions](../com.aspose.words/joinrunsoptions/) | Fournit des indicateurs de configuration pour l'opération de jointure de runs. |
| [JoinStyle](../com.aspose.words/joinstyle/) | Style de jointure de ligne. |
| [JsonDataLoadOptions](../com.aspose.words/jsondataloadoptions/) | Représente les options pour analyser les données JSON. |
| [JsonDataSource](../com.aspose.words/jsondatasource/) | Fournit l'accès aux données d'un fichier ou d'un flux JSON à utiliser dans un rapport. |
| [JsonSimpleValueParseMode](../com.aspose.words/jsonsimplevalueparsemode/) | Spécifie un mode d'analyse des valeurs simples JSON (null, booléen, nombre, entier et chaîne) lors du chargement du JSON. |
| [JustificationMode](../com.aspose.words/justificationmode/) | Spécifie le réglage de l'espacement des caractères pour un document. |
| [KnownTypeSet](../com.aspose.words/knowntypeset/) | Représente un ensemble non ordonné (c.-à-d. |
| [Language](../com.aspose.words/language/) | Spécifie la langue vers laquelle le texte sera traduit à l'aide de l'IA. |
| [LanguagePreferences](../com.aspose.words/languagepreferences/) | Permet de configurer les préférences de langue. |
| [LayoutCollector](../com.aspose.words/layoutcollector/) | Cette classe permet de calculer les numéros de page des nœuds du document. |
| [LayoutEntityType](../com.aspose.words/layoutentitytype/) | Types des entités de mise en page. |
| [LayoutEnumerator](../com.aspose.words/layoutenumerator/) | Énumère les entités de mise en page d'un document. |
| [LayoutFlow](../com.aspose.words/layoutflow/) | Détermine le flux de la mise en page du texte dans une zone de texte. |
| [LayoutOptions](../com.aspose.words/layoutoptions/) | Contient les options qui permettent de contrôler le processus de mise en page du document. |
| [LegendPosition](../com.aspose.words/legendposition/) | Spécifie les positions possibles pour la légende d'un graphique. |
| [License](../com.aspose.words/license/) | Fournit des méthodes pour licencier le composant. |
| [LineNumberRestartMode](../com.aspose.words/linenumberrestartmode/) | Détermine quand la numérotation automatique des lignes redémarre. |
| [LineSpacingRule](../com.aspose.words/linespacingrule/) | Spécifie les valeurs d'espacement des lignes pour un paragraphe. |
| [LineStyle](../com.aspose.words/linestyle/) | Spécifie le style de ligne d'une [Border](../com.aspose.words/border/). |
| [List](../com.aspose.words/list/) | Représente le formatage d'une liste. |
| [ListCollection](../com.aspose.words/listcollection/) | Stocke et gère le formatage des listes à puces et numérotées utilisées dans un document. |
| [ListFormat](../com.aspose.words/listformat/) | Permet de contrôler le formatage de liste appliqué à un paragraphe. |
| [ListLabel](../com.aspose.words/listlabel/) | Définit les propriétés spécifiques à une étiquette de liste. |
| [ListLevel](../com.aspose.words/listlevel/) | Définit le formatage d'un niveau de liste. |
| [ListLevelAlignment](../com.aspose.words/listlevelalignment/) | Spécifie l'alignement du numéro ou du puce de la liste. |
| [ListLevelCollection](../com.aspose.words/listlevelcollection/) | Une collection de formatage de liste pour chaque niveau d'une liste. |
| [ListTemplate](../com.aspose.words/listtemplate/) | Spécifie l'un des formats de liste prédéfinis disponibles dans Microsoft Word. |
| [ListTrailingCharacter](../com.aspose.words/listtrailingcharacter/) | Spécifie le caractère qui sépare l'étiquette de liste du texte du paragraphe. |
| [LoadFormat](../com.aspose.words/loadformat/) | Indique le format du document qui doit être chargé. |
| [LoadOptions](../com.aspose.words/loadoptions/) | Permet de spécifier des options supplémentaires (telles que le mot de passe ou l'URI de base) lors du chargement d'un document dans un objet [Document](../com.aspose.words/document/). |
| [MailMerge](../com.aspose.words/mailmerge/) | Représente la fonctionnalité de publipostage. |
| [MailMergeCheckErrors](../com.aspose.words/mailmergecheckerrors/) | Spécifie comment Microsoft Word signalera les erreurs détectées pendant le publipostage. |
| [MailMergeCleanupOptions](../com.aspose.words/mailmergecleanupoptions/) | Spécifie les options qui déterminent quels éléments sont supprimés pendant le publipostage. |
| [MailMergeDataSource](../com.aspose.words/mailmergedatasource/) | Source de données de publipostage utilisée dans [MailMergerContext](../com.aspose.words/mailmergercontext/). |
| [MailMergeDataType](../com.aspose.words/mailmergedatatype/) | Spécifie le type d'une source de données de publipostage externe. |
| [MailMergeDestination](../com.aspose.words/mailmergedestination/) | Spécifie les résultats possibles qui peuvent être générés lorsqu'un publipostage est effectué sur un document. |
| [MailMergeMainDocumentType](../com.aspose.words/mailmergemaindocumenttype/) | Spécifie les types possibles pour un document source de publipostage. |
| [MailMergeOptions](../com.aspose.words/mailmergeoptions/) | Représente les options de la fonctionnalité de publipostage. |
| [MailMergeRegionInfo](../com.aspose.words/mailmergeregioninfo/) | Contient des informations sur une région de fusion de courrier. |
| [MailMergeSettings](../com.aspose.words/mailmergesettings/) | Spécifie toutes les informations de fusion de courrier pour un document. |
| [MailMerger](../com.aspose.words/mailmerger/) | Fournit des méthodes destinées à remplir le modèle avec des données en utilisant la fusion de courrier simple et les opérations de fusion de courrier avec régions. |
| [MailMergerContext](../com.aspose.words/mailmergercontext/) | Contexte de fusion de courrier. |
| [MappedDataFieldCollection](../com.aspose.words/mappeddatafieldcollection/) | Permet de mapper automatiquement les noms des champs de votre source de données aux noms des champs de fusion de courrier dans le document. |
| [Margins](../com.aspose.words/margins/) | Spécifie les marges prédéfinies. |
| [MarkdownEmptyParagraphExportMode](../com.aspose.words/markdownemptyparagraphexportmode/) | Spécifie comment Aspose.Words exporte les paragraphes vides vers Markdown. |
| [MarkdownExportAsHtml](../com.aspose.words/markdownexportashtml/) | Permet de spécifier les éléments à exporter vers Markdown en tant que HTML brut. |
| [MarkdownLinkExportMode](../com.aspose.words/markdownlinkexportmode/) | Spécifie comment les liens sont exportés vers Markdown. |
| [MarkdownListExportMode](../com.aspose.words/markdownlistexportmode/) | Spécifie comment les listes sont exportées vers Markdown. |
| [MarkdownLoadOptions](../com.aspose.words/markdownloadoptions/) | Permet de spécifier des options supplémentaires lors du chargement d'un document [LoadFormat.\#MARKDOWN](../com.aspose.words/loadformat/\#MARKDOWN) dans un objet [Document](../com.aspose.words/document/). |
| [MarkdownOfficeMathExportMode](../com.aspose.words/markdownofficemathexportmode/) | Spécifie comment Aspose.Words exporte OfficeMath vers Markdown. |
| [MarkdownSaveOptions](../com.aspose.words/markdownsaveoptions/) | Classe permettant de spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#MARKDOWN](../com.aspose.words/saveformat/\#MARKDOWN). |
| [MarkerSymbol](../com.aspose.words/markersymbol/) | Spécifie le style du symbole du marqueur. |
| [MarkupLevel](../com.aspose.words/markuplevel/) | Spécifie le niveau dans l'arborescence du document où une [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/) particulière peut apparaître. |
| [MathObjectType](../com.aspose.words/mathobjecttype/) | Spécifie le type d'un objet Office Math. |
| [MeasurementUnits](../com.aspose.words/measurementunits/) | Spécifie l'unité de mesure. |
| [MemoryFontSource](../com.aspose.words/memoryfontsource/) | Représente le fichier de police TrueType unique stocké en mémoire. |
| [MergeFieldImageDimension](../com.aspose.words/mergefieldimagedimension/) | Représente une dimension d'image (c.-à-d. |
| [MergeFieldImageDimensionUnit](../com.aspose.words/mergefieldimagedimensionunit/) | Spécifie une unité d'une dimension d'image (c.-à-d. |
| [MergeFormatMode](../com.aspose.words/mergeformatmode/) | Spécifie comment le formatage est fusionné lors de la combinaison de plusieurs documents. |
| [Merger](../com.aspose.words/merger/) | Représente un groupe de méthodes destinées à fusionner une variété de types de documents différents en un seul document de sortie. |
| [MergerContext](../com.aspose.words/mergercontext/) | Contexte du fusionneur de documents. |
| [MetafileRenderingMode](../com.aspose.words/metafilerenderingmode/) | Spécifie comment Aspose.Words doit rendre les métafichiers WMF et EMF. |
| [MetafileRenderingOptions](../com.aspose.words/metafilerenderingoptions/) | Permet de spécifier des options supplémentaires de rendu des métafichiers. |
| [Metered](../com.aspose.words/metered/) | Fournit des méthodes pour définir la clé mesurée. |
| [MorphDataControl](../com.aspose.words/morphdatacontrol/) | La structure MorphDataControl est un agrégat de six contrôles : CheckBox, ComboBox, ListBox, OptionButton, TextBox et ToggleButton. |
| [MsWordVersion](../com.aspose.words/mswordversion/) | Permet à Aspose.Wods d'imiter le comportement de l'application propre à chaque version de MS Word. |
| [MultiPageLayout](../com.aspose.words/multipagelayout/) | Définit une mise en page pour le rendu de plusieurs pages en une seule sortie. |
| [MultiplePagesType](../com.aspose.words/multiplepagestype/) | Spécifie comment le document est imprimé. |
| [MustacheTag](../com.aspose.words/mustachetag/) | Représente la balise "mustache". |
| [NativeLibSettings](../com.aspose.words/nativelibsettings/) | Cette classe aide à définir diverses options telles que le dossier temporaire pour les bibliothèques natives d'Aspose.Words et si les bibliothèques natives doivent être chargées et utilisées. |
| [Node](../com.aspose.words/node/) | Classe de base pour tous les nœuds d'un document Word. |
| [NodeChangingAction](../com.aspose.words/nodechangingaction/) | Spécifie le type de modification de nœud. |
| [NodeChangingArgs](../com.aspose.words/nodechangingargs/) | Fournit des données pour les méthodes de l'interface [INodeChangingCallback](../com.aspose.words/inodechangingcallback/). |
| [NodeCollection](../com.aspose.words/nodecollection/) | Représente une collection de nœuds d'un type spécifique. |
| [NodeImporter](../com.aspose.words/nodeimporter/) | Permet d'effectuer efficacement des importations répétées de nœuds d'un document à un autre. |
| [NodeList](../com.aspose.words/nodelist/) | Représente une collection de nœuds correspondant à une requête XPath exécutée à l'aide de la méthode [CompositeNode.\#selectNodes(java.lang.String)](../com.aspose.words/compositenode/\#selectNodes-java.lang.String). |
| [NodeRendererBase](../com.aspose.words/noderendererbase/) | Classe de base pour [ShapeRenderer](../com.aspose.words/shaperenderer/) et [OfficeMathRenderer](../com.aspose.words/officemathrenderer/). |
| [NodeType](../com.aspose.words/nodetype/) | Spécifie le type d'un nœud de document Word. |
| [NumSpacing](../com.aspose.words/numspacing/) | Spécifie les valeurs possibles dans lesquelles l'espacement des chiffres peut être affiché. |
| [NumberStyle](../com.aspose.words/numberstyle/) | Spécifie le style de numérotation pour une liste, les notes de bas de page et les notes de fin, ainsi que les numéros de page. |
| [NumeralFormat](../com.aspose.words/numeralformat/) | Indique le jeu de symboles utilisé pour représenter les nombres lors du rendu vers des formats de page fixes. |
| [Odso](../com.aspose.words/odso/) | Spécifie les paramètres de l'Office Data Source Object (ODSO) pour une source de données de publipostage. |
| [OdsoDataSourceType](../com.aspose.words/odsodatasourcetype/) | Spécifie le type de la source de données externe à connecter dans le cadre des informations de connexion ODSO. |
| [OdsoFieldMapData](../com.aspose.words/odsofieldmapdata/) | Spécifie comment une colonne de la source de données externe doit être mappée aux champs de fusion prédéfinis du document. |
| [OdsoFieldMapDataCollection](../com.aspose.words/odsofieldmapdatacollection/) | Une collection typée des objets [OdsoFieldMapData](../com.aspose.words/odsofieldmapdata/). |
| [OdsoFieldMappingType](../com.aspose.words/odsofieldmappingtype/) | Spécifie les types possibles utilisés pour indiquer si un champ de publipostage donné a été mappé à une colonne de la source de données externe donnée. |
| [OdsoRecipientData](../com.aspose.words/odsorecipientdata/) | Représente les informations concernant un enregistrement unique d'une source de données externe qui doit être exclu du publipostage. |
| [OdsoRecipientDataCollection](../com.aspose.words/odsorecipientdatacollection/) | Une collection typée de [OdsoRecipientData](../com.aspose.words/odsorecipientdata/) |
| [OdtSaveMeasureUnit](../com.aspose.words/odtsavemeasureunit/) | Unités de mesure spécifiées à appliquer au contenu mesurable du document tel que les formes, les largeurs et autres lors de l'enregistrement. |
| [OdtSaveOptions](../com.aspose.words/odtsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.#ODT](../com.aspose.words/saveformat/#ODT) ou [SaveFormat.#OTT](../com.aspose.words/saveformat/#OTT). |
| [OfficeMath](../com.aspose.words/officemath/) | Représente un objet Office Math tel qu'une fonction, une équation, une matrice ou similaire. |
| [OfficeMathDisplayType](../com.aspose.words/officemathdisplaytype/) | Spécifie le type de format d'affichage de l'équation. |
| [OfficeMathJustification](../com.aspose.words/officemathjustification/) | Spécifie l'alignement de l'équation. |
| [OfficeMathRenderer](../com.aspose.words/officemathrenderer/) | Fournit des méthodes pour rendre un [OfficeMath](../com.aspose.words/officemath/) individuel en image raster ou vectorielle ou vers un objet Graphics. |
| [OleControl](../com.aspose.words/olecontrol/) | Représente le contrôle OLE ActiveX. |
| [OleFormat](../com.aspose.words/oleformat/) | Fournit l'accès aux données d'un objet OLE ou d'un contrôle ActiveX. |
| [OlePackage](../com.aspose.words/olepackage/) | Permet d'accéder aux propriétés du package OLE. |
| [OoxmlCompliance](../com.aspose.words/ooxmlcompliance/) | Permet de spécifier quelle spécification OOXML sera utilisée lors de l'enregistrement au format DOCX. |
| [OoxmlSaveOptions](../com.aspose.words/ooxmlsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.#DOCX](../com.aspose.words/saveformat/#DOCX), [SaveFormat.#DOCM](../com.aspose.words/saveformat/#DOCM), [SaveFormat.#DOTX](../com.aspose.words/saveformat/#DOTX), [SaveFormat.#DOTM](../com.aspose.words/saveformat/#DOTM) ou [SaveFormat.#FLAT_OPC](../com.aspose.words/saveformat/#FLAT-OPC). |
| [OpenAiModel](../com.aspose.words/openaimodel/) | Classe représentant l'intégration des modèles OpenAi au sein d'Aspose.Words. |
| [OptionButtonControl](../com.aspose.words/optionbuttoncontrol/) | Le contrôle OptionButton permet un choix unique dans un ensemble limité de choix mutuellement exclusifs. |
| [Orientation](../com.aspose.words/orientation/) | Spécifie l'orientation de la page. |
| [OutlineLevel](../com.aspose.words/outlinelevel/) | Spécifie le niveau de plan d'un paragraphe dans le document. |
| [OutlineOptions](../com.aspose.words/outlineoptions/) | Permet de spécifier les options de plan. |
| [PageBorderAppliesTo](../com.aspose.words/pageborderappliesto/) | Spécifie sur quelles pages la bordure de page est imprimée. |
| [PageBorderDistanceFrom](../com.aspose.words/pageborderdistancefrom/) | Spécifie le positionnement de la bordure de page par rapport à la marge de la page. |
| [PageExtractOptions](../com.aspose.words/pageextractoptions/) | Permet de spécifier les options d'extraction des pages du document. |
| [PageInfo](../com.aspose.words/pageinfo/) | Représente les informations concernant une page de document particulière. |
| [PageLayoutCallbackArgs](../com.aspose.words/pagelayoutcallbackargs/) | Un argument passé à [IPageLayoutCallback.#notify(com.aspose.words.PageLayoutCallbackArgs)](../com.aspose.words/ipagelayoutcallback/#notify-com.aspose.words.PageLayoutCallbackArgs) |
| [PageLayoutEvent](../com.aspose.words/pagelayoutevent/) | Un code d'événement déclenché lors de la construction et du rendu du modèle de mise en page. |
| [PageRange](../com.aspose.words/pagerange/) | Représente une plage continue de pages. |
| [PageSavingArgs](../com.aspose.words/pagesavingargs/) | Fournit des données pour l'événement [IPageSavingCallback.#pageSaving(com.aspose.words.PageSavingArgs)](../com.aspose.words/ipagesavingcallback/#pageSaving-com.aspose.words.PageSavingArgs). |
| [PageSet](../com.aspose.words/pageset/) | Décrit un ensemble aléatoire de pages. |
| [PageSetup](../com.aspose.words/pagesetup/) | Représente les propriétés de configuration de page d'une section. |
| [PageVerticalAlignment](../com.aspose.words/pageverticalalignment/) | Spécifie la justification verticale du texte sur chaque page. |
| [PaperSize](../com.aspose.words/papersize/) | Spécifie la taille du papier. |
| [Paragraph](../com.aspose.words/paragraph/) | Représente un paragraphe de texte. |
| [ParagraphAlignment](../com.aspose.words/paragraphalignment/) | Spécifie l'alignement du texte dans un paragraphe. |
| [ParagraphCollection](../com.aspose.words/paragraphcollection/) | Fournit un accès typé à une collection de nœuds [Paragraph](../com.aspose.words/paragraph/). |
| [ParagraphFormat](../com.aspose.words/paragraphformat/) | Représente toute la mise en forme d'un paragraphe. |
| [PatternType](../com.aspose.words/patterntype/) | Spécifie le motif de remplissage à utiliser pour remplir une forme. |
| [PclSaveOptions](../com.aspose.words/pclsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#PCL](../com.aspose.words/saveformat/\#PCL). |
| [PdfAttachmentsEmbeddingMode](../com.aspose.words/pdfattachmentsembeddingmode/) | Spécifie comment les pièces jointes sont incorporées dans le document PDF. |
| [PdfCompliance](../com.aspose.words/pdfcompliance/) | Spécifie le niveau de conformité aux normes PDF. |
| [PdfCustomPropertiesExport](../com.aspose.words/pdfcustompropertiesexport/) | Spécifie la manière dont [Document.\#getCustomDocumentProperties()](../com.aspose.words/document/\#getCustomDocumentProperties) sont exportées vers le fichier PDF. |
| [PdfDigitalSignatureDetails](../com.aspose.words/pdfdigitalsignaturedetails/) | Contient les détails pour signer un document PDF avec une signature numérique. |
| [PdfDigitalSignatureHashAlgorithm](../com.aspose.words/pdfdigitalsignaturehashalgorithm/) | Spécifie un algorithme de hachage numérique utilisé par une signature numérique. |
| [PdfDigitalSignatureTimestampSettings](../com.aspose.words/pdfdigitalsignaturetimestampsettings/) | Contient les paramètres de l'horodatage de la signature numérique. |
| [PdfEncryptionDetails](../com.aspose.words/pdfencryptiondetails/) | Contient les détails du chiffrement et des autorisations d'accès pour un document PDF. |
| [PdfFontEmbeddingMode](../com.aspose.words/pdffontembeddingmode/) | Spécifie comment Aspose.Words doit incorporer les polices. |
| [PdfImageColorSpaceExportMode](../com.aspose.words/pdfimagecolorspaceexportmode/) | Spécifie comment l'espace colorimétrique sera sélectionné pour les images dans le document PDF. |
| [PdfImageCompression](../com.aspose.words/pdfimagecompression/) | Spécifie le type de compression appliqué aux images dans le fichier PDF. |
| [PdfLoadOptions](../com.aspose.words/pdfloadoptions/) | Permet de spécifier des options supplémentaires lors du chargement d'un document Pdf dans un objet [Document](../com.aspose.words/document/). |
| [PdfPageLayout](../com.aspose.words/pdfpagelayout/) | Spécifie la mise en page à utiliser lorsque le document est ouvert dans un lecteur PDF. |
| [PdfPageMode](../com.aspose.words/pdfpagemode/) | Spécifie comment le document PDF doit être affiché lorsqu'il est ouvert dans le lecteur PDF. |
| [PdfPermissions](../com.aspose.words/pdfpermissions/) | Spécifie les opérations autorisées à un utilisateur sur un document PDF chiffré. |
| [PdfSaveOptions](../com.aspose.words/pdfsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#PDF](../com.aspose.words/saveformat/\#PDF). |
| [PdfTextCompression](../com.aspose.words/pdftextcompression/) | Spécifie un type de compression appliqué à tout le contenu du fichier PDF, sauf les images. |
| [PdfZoomBehavior](../com.aspose.words/pdfzoombehavior/) | Spécifie le type de zoom appliqué à un document PDF lorsqu'il est ouvert dans un visualiseur PDF. |
| [Person](../com.aspose.words/person/) | Représente un contributeur individuel (une personne) d'une source bibliographique. |
| [PersonCollection](../com.aspose.words/personcollection/) | Représente une liste de personnes qui sont des contributeurs de sources bibliographiques. |
| [PhoneticGuide](../com.aspose.words/phoneticguide/) | Représente le Guide phonétique. |
| [PhysicalFontInfo](../com.aspose.words/physicalfontinfo/) | Spécifie les informations sur la police physique disponible pour le moteur de polices Aspose.Words. |
| [PlainTextDocument](../com.aspose.words/plaintextdocument/) | Permet d'extraire la représentation en texte brut du contenu du document. |
| [PreferredWidth](../com.aspose.words/preferredwidth/) | Représente une valeur et son unité de mesure utilisées pour spécifier la largeur préférée d'un tableau ou d'une cellule. |
| [PreferredWidthType](../com.aspose.words/preferredwidthtype/) | Spécifie l'unité de mesure de la largeur préférée d'un tableau ou d'une cellule. |
| [PresetTexture](../com.aspose.words/presettexture/) | Spécifie la texture à utiliser pour remplir une forme. |
| [Processor](../com.aspose.words/processor/) | Classe de processeur pour exécuter différentes actions de traitement de documents. |
| [ProcessorContext](../com.aspose.words/processorcontext/) | Classe de base pour les contextes de processeur. |
| [PropertyType](../com.aspose.words/propertytype/) | Spécifie le type de données d'une propriété de document. |
| [ProtectionType](../com.aspose.words/protectiontype/) | Type de protection d'un document. |
| [PsSaveOptions](../com.aspose.words/pssaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.#PS](../com.aspose.words/saveformat/#PS). |
| [Range](../com.aspose.words/range/) | Représente une zone contiguë dans un document. |
| [ReadabilityStatistics](../com.aspose.words/readabilitystatistics/) | Fournit des informations sur le score de lisibilité du document. |
| [ReflectionFormat](../com.aspose.words/reflectionformat/) | Représente le formatage de réflexion pour un objet. |
| [RelativeHorizontalPosition](../com.aspose.words/relativehorizontalposition/) | Spécifie par rapport à quoi la position horizontale d'une forme ou d'un cadre de texte est relative. |
| [RelativeHorizontalSize](../com.aspose.words/relativehorizontalsize/) | Spécifie relativement à quoi la largeur d'une forme ou d'un cadre de texte est calculée horizontalement. |
| [RelativeVerticalPosition](../com.aspose.words/relativeverticalposition/) | Spécifie par rapport à quoi la position verticale d'une forme ou d'un cadre de texte est relative. |
| [RelativeVerticalSize](../com.aspose.words/relativeverticalsize/) | Spécifie relativement à quoi la hauteur d'une forme ou d'un cadre de texte est calculée verticalement. |
| [ReplaceAction](../com.aspose.words/replaceaction/) | Permet à l'utilisateur de spécifier ce qui arrive à la correspondance actuelle pendant une opération de remplacement. |
| [ReplacementFormat](../com.aspose.words/replacementformat/) | Spécifie le format de remplacement. |
| [Replacer](../com.aspose.words/replacer/) | Fournit des méthodes destinées à rechercher et remplacer du texte dans le document. |
| [ReplacerContext](../com.aspose.words/replacercontext/) | Contexte d'opération de recherche/remplacement. |
| [ReplacingArgs](../com.aspose.words/replacingargs/) | Fournit des données pour une opération de remplacement personnalisée. |
| [ReportBuildOptions](../com.aspose.words/reportbuildoptions/) | Spécifie les options contrôlant le comportement de [ReportingEngine](../com.aspose.words/reportingengine/) lors de la génération d'un rapport. |
| [ReportBuilder](../com.aspose.words/reportbuilder/) | Fournit des méthodes destinées à remplir le modèle avec des données en utilisant LINQ Reporting Engine. |
| [ReportBuilderContext](../com.aspose.words/reportbuildercontext/) | Contexte de LINQ Reporting Engine. |
| [ReportBuilderOptions](../com.aspose.words/reportbuilderoptions/) | Représente les options pour la fonctionnalité de LINQ Reporting Engine. |
| [ReportingEngine](../com.aspose.words/reportingengine/) | Fournit des routines pour remplir les documents modèles avec des données ainsi qu'un ensemble de paramètres pour contrôler ces routines. |
| [ResourceLoadingAction](../com.aspose.words/resourceloadingaction/) | Spécifie le mode de chargement des ressources. |
| [ResourceLoadingArgs](../com.aspose.words/resourceloadingargs/) | Fournit des données pour la méthode [IResourceLoadingCallback.#resourceLoading(com.aspose.words.ResourceLoadingArgs)](../com.aspose.words/iresourceloadingcallback/#resourceLoading-com.aspose.words.ResourceLoadingArgs). |
| [ResourceSavingArgs](../com.aspose.words/resourcesavingargs/) | Fournit des données pour l'événement [IResourceSavingCallback.#resourceSaving(com.aspose.words.ResourceSavingArgs)](../com.aspose.words/iresourcesavingcallback/#resourceSaving-com.aspose.words.ResourceSavingArgs). |
| [ResourceType](../com.aspose.words/resourcetype/) | Type de ressource chargée. |
| [Revision](../com.aspose.words/revision/) | Représente une révision (modification suivie) dans un nœud ou un style de document. |
| [RevisionCollection](../com.aspose.words/revisioncollection/) | Une collection d'objets [Revision](../com.aspose.words/revision/) qui représentent les révisions dans le document. |
| [RevisionColor](../com.aspose.words/revisioncolor/) | Permet de spécifier la couleur des révisions du document. |
| [RevisionGroup](../com.aspose.words/revisiongroup/) | Représente un groupe d'objets [Revision](../com.aspose.words/revision/) séquentiels. |
| [RevisionGroupCollection](../com.aspose.words/revisiongroupcollection/) | Une collection d'objets [RevisionGroup](../com.aspose.words/revisiongroup/) qui représentent les groupes de révisions dans le document. |
| [RevisionOptions](../com.aspose.words/revisionoptions/) | Permet de contrôler la façon dont les révisions du document sont gérées pendant le processus de mise en page. |
| [RevisionTextEffect](../com.aspose.words/revisiontexteffect/) | Permet de spécifier l'effet de décoration pour les révisions du texte du document. |
| [RevisionType](../com.aspose.words/revisiontype/) | Spécifie le type de modification suivie dans [Revision](../com.aspose.words/revision/). |
| [RevisionsView](../com.aspose.words/revisionsview/) | Permet de spécifier s'il faut travailler avec la version originale ou révisée d'un document. |
| [Row](../com.aspose.words/row/) | Représente une ligne de tableau. |
| [RowCollection](../com.aspose.words/rowcollection/) | Fournit un accès typé à une collection de nœuds [Row](../com.aspose.words/row/). |
| [RowFormat](../com.aspose.words/rowformat/) | Représente toute la mise en forme d'une ligne de tableau. |
| [RtfLoadOptions](../com.aspose.words/rtfloadoptions/) | Permet de spécifier des options supplémentaires lors du chargement d'un document [LoadFormat.#RTF](../com.aspose.words/loadformat/#RTF) dans un objet [Document](../com.aspose.words/document/). |
| [RtfSaveOptions](../com.aspose.words/rtfsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.#RTF](../com.aspose.words/saveformat/#RTF). |
| [Run](../com.aspose.words/run/) | Représente une séquence de caractères avec la même mise en forme de police. |
| [RunCollection](../com.aspose.words/runcollection/) | Fournit un accès typé à une collection de nœuds [Run](../com.aspose.words/run/). |
| [SaveFormat](../com.aspose.words/saveformat/) | Indique le format dans lequel le document est enregistré. |
| [SaveOptions](../com.aspose.words/saveoptions/) | Il s'agit d'une classe de base abstraite pour les classes qui permettent à l'utilisateur de spécifier des options supplémentaires lors de l'enregistrement d'un document dans un format particulier. |
| [SaveOutputParameters](../com.aspose.words/saveoutputparameters/) | Cet objet est renvoyé à l'appelant après l'enregistrement d'un document et contient des informations supplémentaires qui ont été générées ou calculées pendant l'opération d'enregistrement. |
| [ScriptShapingLevel](../com.aspose.words/scriptshapinglevel/) | Décrit les niveaux de mise en forme requis par un script. |
| [SdtAppearance](../com.aspose.words/sdtappearance/) | Spécifie l'apparence d'une balise de document structuré. |
| [SdtCalendarType](../com.aspose.words/sdtcalendartype/) | Spécifie les types de calendriers possibles qui peuvent être utilisés pour spécifier [StructuredDocumentTag.\#getCalendarType()](../com.aspose.words/structureddocumenttag/\#getCalendarType) / [StructuredDocumentTag.\#setCalendarType(int)](../com.aspose.words/structureddocumenttag/\#setCalendarType-int) dans un document Office Open XML. |
| [SdtDateStorageFormat](../com.aspose.words/sdtdatestorageformat/) | Spécifie comment la date d'un SDT de type date est stockée/récupérée lorsque le SDT est lié à un nœud XML dans le magasin de données du document. |
| [SdtListItem](../com.aspose.words/sdtlistitem/) | Cet élément spécifie un seul élément de liste au sein d'une balise de document structuré parent [SdtType.\#COMBO\_BOX](../com.aspose.words/sdttype/\#COMBO-BOX) ou [SdtType.\#DROP\_DOWN\_LIST](../com.aspose.words/sdttype/\#DROP-DOWN-LIST). |
| [SdtListItemCollection](../com.aspose.words/sdtlistitemcollection/) | Fournit un accès aux éléments [SdtListItem](../com.aspose.words/sdtlistitem/) d'une balise de document structuré. |
| [SdtType](../com.aspose.words/sdttype/) | Spécifie le type d'un nœud de balise de document structuré (SDT). |
| [Section](../com.aspose.words/section/) | Représente une seule section dans un document. |
| [SectionCollection](../com.aspose.words/sectioncollection/) | Une collection d'objets [Section](../com.aspose.words/section/) dans le document. |
| [SectionLayoutMode](../com.aspose.words/sectionlayoutmode/) | Spécifie le mode de mise en page d'une section permettant de définir le comportement de la grille du document. |
| [SectionStart](../com.aspose.words/sectionstart/) | Le type de saut au début de la section. |
| [Shading](../com.aspose.words/shading/) | Contient les attributs d'ombrage pour un objet. |
| [ShadowFormat](../com.aspose.words/shadowformat/) | Représente le format d'ombre pour un objet. |
| [ShadowType](../com.aspose.words/shadowtype/) | Spécifie le type d'ombre d'une forme. |
| [Shape](../com.aspose.words/shape/) | Représente un objet dans le calque de dessin, tel qu'une AutoShape, une zone de texte, une forme libre, un objet OLE, un contrôle ActiveX ou une image. |
| [ShapeBase](../com.aspose.words/shapebase/) | Classe de base pour les objets du calque de dessin, tels qu'une AutoShape, une forme libre, un objet OLE, un contrôle ActiveX ou une image. |
| [ShapeLineStyle](../com.aspose.words/shapelinestyle/) | Spécifie le style de ligne composé d'une [Shape](../com.aspose.words/shape/). |
| [ShapeMarkupLanguage](../com.aspose.words/shapemarkuplanguage/) | Spécifie le langage de balisage utilisé pour la forme. |
| [ShapeRenderer](../com.aspose.words/shaperenderer/) | Fournit des méthodes pour rendre une [Shape](../com.aspose.words/shape/) ou une [GroupShape](../com.aspose.words/groupshape/) individuelle en image raster ou vectorielle ou dans un objet Graphics. |
| [ShapeTextOrientation](../com.aspose.words/shapetextorientation/) | Spécifie l'orientation du texte dans les formes. |
| [ShapeType](../com.aspose.words/shapetype/) | Spécifie le type de forme dans un document Microsoft Word. |
| [ShowInBalloons](../com.aspose.words/showinballoons/) | Spécifie quelles révisions sont rendues dans des bulles. |
| [SignOptions](../com.aspose.words/signoptions/) | Permet de spécifier les options pour la signature de documents. |
| [SignatureLine](../com.aspose.words/signatureline/) | Fournit l'accès aux propriétés de la ligne de signature. |
| [SignatureLineOptions](../com.aspose.words/signaturelineoptions/) | Permet de spécifier les options pour l'insertion d'une ligne de signature. |
| [SignerContext](../com.aspose.words/signercontext/) | Contexte du signataire du document |
| [SmartTag](../com.aspose.words/smarttag/) | Cet élément spécifie la présence d'une balise intelligente autour d'une ou plusieurs structures en ligne (segments, images, champs, etc.) dans un paragraphe. |
| [SoftEdgeFormat](../com.aspose.words/softedgeformat/) | Représente le formatage à bord doux pour un objet. |
| [Source](../com.aspose.words/source/) | Représente une source individuelle, telle qu'un livre, un article de revue ou une interview. |
| [SourceType](../com.aspose.words/sourcetype/) | Représente les types de sources bibliographiques. |
| [SpecialChar](../com.aspose.words/specialchar/) | Classe de base pour les caractères spéciaux dans le document. |
| [SplitCriteria](../com.aspose.words/splitcriteria/) | Spécifie comment le document est découpé en parties. |
| [SplitOptions](../com.aspose.words/splitoptions/) | Spécifie les options de découpage du document en parties. |
| [Splitter](../com.aspose.words/splitter/) | Fournit des méthodes destinées à découper les documents en parties en utilisant différents critères. |
| [SplitterContext](../com.aspose.words/splittercontext/) | Contexte du découpeur de documents. |
| [Story](../com.aspose.words/story/) | Classe de base pour les éléments qui contiennent des nœuds de niveau bloc [Paragraph](../com.aspose.words/paragraph/) et [Table](../com.aspose.words/table/). |
| [StoryType](../com.aspose.words/storytype/) | Le texte d'un document Word est stocké dans des récits. |
| [StreamFontSource](../com.aspose.words/streamfontsource/) | Classe de base pour la source de police de flux définie par l'utilisateur. |
| [Stroke](../com.aspose.words/stroke/) | Définit un trait pour une forme. |
| [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/) | Représente une balise de document structuré (SDT ou contrôle de contenu) dans un document. |
| [StructuredDocumentTagCollection](../com.aspose.words/structureddocumenttagcollection/) | Une collection d'instances [IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag/) qui représentent les balises de document structuré dans la plage spécifiée. |
| [StructuredDocumentTagRangeEnd](../com.aspose.words/structureddocumenttagrangeend/) | Représente la fin d'une balise de document structuré **ranged** qui accepte du contenu multi‑sections. |
| [StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart/) | Représente le début d'une balise de document structuré **ranged** qui accepte du contenu multi‑sections. |
| [Style](../com.aspose.words/style/) | Représente un style unique intégré ou défini par l'utilisateur. |
| [StyleCollection](../com.aspose.words/stylecollection/) | Une collection d'objets [Style](../com.aspose.words/style/) qui représentent à la fois les styles intégrés et définis par l'utilisateur dans un document. |
| [StyleIdentifier](../com.aspose.words/styleidentifier/) | Identifiant de style indépendant de la locale. |
| [StyleType](../com.aspose.words/styletype/) | Représente le type du style. |
| [SubDocument](../com.aspose.words/subdocument/) | Représente un **SubDocument** \- qui est une référence à un document stocké à l'extérieur. |
| [SummarizeOptions](../com.aspose.words/summarizeoptions/) | Permet de spécifier diverses options pour résumer le contenu du document. |
| [SummaryLength](../com.aspose.words/summarylength/) | Énumère les longueurs possibles du résumé. |
| [SuperUserJwtTokenRequestHandler](../com.aspose.words/superuserjwttokenrequesthandler/) | Gestionnaire de requêtes de jeton JWT avec mise en cache, validation locale et disjoncteur. |
| [SvgSaveOptions](../com.aspose.words/svgsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#SVG](../com.aspose.words/saveformat/\#SVG). |
| [SvgTextOutputMode](../com.aspose.words/svgtextoutputmode/) | Permet de spécifier comment le texte à l'intérieur d'un document doit être rendu lors de l'enregistrement au format SVG. |
| [SystemFontSource](../com.aspose.words/systemfontsource/) | Représente toutes les polices TrueType installées sur le système. |
| [TabAlignment](../com.aspose.words/tabalignment/) | Spécifie l'alignement/type d'un arrêt de tabulation. |
| [TabLeader](../com.aspose.words/tableader/) | Spécifie le type de la ligne de repère affichée sous le caractère de tabulation. |
| [TabStop](../com.aspose.words/tabstop/) | Représente un arrêt de tabulation personnalisé unique. |
| [TabStopCollection](../com.aspose.words/tabstopcollection/) | Une collection d'objets [TabStop](../com.aspose.words/tabstop/) qui représentent des tabulations personnalisées pour un paragraphe ou un style. |
| [Table](../com.aspose.words/table/) | Représente un tableau dans un document Word. |
| [TableAlignment](../com.aspose.words/tablealignment/) | Spécifie l'alignement d'un tableau en ligne. |
| [TableCollection](../com.aspose.words/tablecollection/) | Fournit un accès typé à une collection de nœuds [Table](../com.aspose.words/table/). |
| [TableContentAlignment](../com.aspose.words/tablecontentalignment/) | Permet de spécifier l'alignement du contenu du tableau à utiliser lors de l'exportation au format Markdown. |
| [TableStyle](../com.aspose.words/tablestyle/) | Représente un style de tableau. |
| [TableStyleOptions](../com.aspose.words/tablestyleoptions/) | Spécifie comment le style de tableau est appliqué à un tableau. |
| [TableSubstitutionRule](../com.aspose.words/tablesubstitutionrule/) | Règle de substitution de police du tableau. |
| [TaskPane](../com.aspose.words/taskpane/) | Représente un objet de volet de tâche d'extension. |
| [TaskPaneCollection](../com.aspose.words/taskpanecollection/) | Spécifie une liste d'objets de volet de tâche persistés. |
| [TaskPaneDockState](../com.aspose.words/taskpanedockstate/) | Énumère les emplacements disponibles de l'objet de volet de tâche. |
| [TextBox](../com.aspose.words/textbox/) | Définit les attributs qui spécifient comment un texte est affiché à l'intérieur d'une forme. |
| [TextBoxAnchor](../com.aspose.words/textboxanchor/) | Spécifie les valeurs utilisées pour l'alignement vertical du texte de forme. |
| [TextBoxControl](../com.aspose.words/textboxcontrol/) | Le contrôle TextBox affiche du texte provenant d'un ensemble organisé de données ou d'une saisie utilisateur. |
| [TextBoxWrapMode](../com.aspose.words/textboxwrapmode/) | Spécifie comment le texte s’enroule à l’intérieur d’une forme. |
| [TextColumn](../com.aspose.words/textcolumn/) | Représente une seule colonne de texte. |
| [TextColumnCollection](../com.aspose.words/textcolumncollection/) | Une collection d’objets [TextColumn](../com.aspose.words/textcolumn/) qui représentent toutes les colonnes de texte dans une section d’un document. |
| [TextDmlEffect](../com.aspose.words/textdmleffect/) | Effet de texte Dml pour les séquences de texte. |
| [TextEffect](../com.aspose.words/texteffect/) | Effet d’animation pour les séquences de texte. |
| [TextFormFieldType](../com.aspose.words/textformfieldtype/) | Spécifie le type d’un champ de formulaire texte. |
| [TextOrientation](../com.aspose.words/textorientation/) | Spécifie l’orientation du texte sur une page, dans une cellule de tableau ou un cadre de texte. |
| [TextPath](../com.aspose.words/textpath/) | Définit le texte et le formatage du tracé de texte (d’un objet WordArt). |
| [TextPathAlignment](../com.aspose.words/textpathalignment/) | Alignement WordArt. |
| [TextWatermarkOptions](../com.aspose.words/textwatermarkoptions/) | Contient les options qui peuvent être spécifiées lors de l’ajout d’un filigrane avec du texte. |
| [TextWrapping](../com.aspose.words/textwrapping/) | Spécifie comment le texte s’enroule autour du tableau. |
| [TextureAlignment](../com.aspose.words/texturealignment/) | Spécifie l’alignement du carrelage du remplissage de texture. |
| [TextureIndex](../com.aspose.words/textureindex/) | Spécifie la texture d’ombrage. |
| [Theme](../com.aspose.words/theme/) | Représente le thème du document et fournit l’accès aux principales parties du thème, y compris [Theme.#getMajorFonts()](../com.aspose.words/theme/#getMajorFonts), [Theme.#getMinorFonts()](../com.aspose.words/theme/#getMinorFonts) et [Theme.#getColors()](../com.aspose.words/theme/#getColors) |
| [ThemeColor](../com.aspose.words/themecolor/) | Spécifie les couleurs du thème pour les thèmes de document. |
| [ThemeColors](../com.aspose.words/themecolors/) | Représente le schéma de couleurs du thème du document qui contient douze couleurs. |
| [ThemeFont](../com.aspose.words/themefont/) | Spécifie les types de noms de polices du thème pour les thèmes de document. |
| [ThemeFonts](../com.aspose.words/themefonts/) | Représente une collection de polices dans le schéma de polices, permettant de spécifier différentes polices pour différentes langues [ThemeFonts.#getLatin()](../com.aspose.words/themefonts/#getLatin) / [ThemeFonts.#setLatin(java.lang.String)](../com.aspose.words/themefonts/#setLatin-java.lang.String), [ThemeFonts.#getEastAsian()](../com.aspose.words/themefonts/#getEastAsian) / [ThemeFonts.#setEastAsian(java.lang.String)](../com.aspose.words/themefonts/#setEastAsian-java.lang.String) et [ThemeFonts.#getComplexScript()](../com.aspose.words/themefonts/#getComplexScript) / [ThemeFonts.#setComplexScript(java.lang.String)](../com.aspose.words/themefonts/#setComplexScript-java.lang.String). |
| [ThumbnailGeneratingOptions](../com.aspose.words/thumbnailgeneratingoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de la génération d’une vignette pour un document. |
| [TiffCompression](../com.aspose.words/tiffcompression/) | Spécifie le type de compression à appliquer lors de l’enregistrement des images de pages dans un fichier TIFF. |
| [ToaCategories](../com.aspose.words/toacategories/) | Représente un tableau des catégories d’autorités. |
| [TxtExportHeadersFootersMode](../com.aspose.words/txtexportheadersfootersmode/) | Spécifie la manière dont les en-têtes et pieds de page sont exportés au format texte brut. |
| [TxtLeadingSpacesOptions](../com.aspose.words/txtleadingspacesoptions/) | Spécifie les options disponibles pour la gestion des espaces de tête lors de l’importation depuis un fichier [LoadFormat.#TEXT](../com.aspose.words/loadformat/#TEXT). |
| [TxtListIndentation](../com.aspose.words/txtlistindentation/) | Spécifie comment les niveaux de liste sont indentés lorsque le document est exporté au format [SaveFormat.#TEXT](../com.aspose.words/saveformat/#TEXT). |
| [TxtLoadOptions](../com.aspose.words/txtloadoptions/) | Permet de spécifier des options supplémentaires lors du chargement d’un document [LoadFormat.#TEXT](../com.aspose.words/loadformat/#TEXT) dans un objet [Document](../com.aspose.words/document/). |
| [TxtOfficeMathExportMode](../com.aspose.words/txtofficemathexportmode/) | Spécifie comment Aspose.Words exporte OfficeMath vers [SaveFormat.\#TEXT](../com.aspose.words/saveformat/\#TEXT). |
| [TxtSaveOptions](../com.aspose.words/txtsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#TEXT](../com.aspose.words/saveformat/\#TEXT). |
| [TxtSaveOptionsBase](../com.aspose.words/txtsaveoptionsbase/) | La classe de base pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans des formats basés sur du texte. |
| [TxtTrailingSpacesOptions](../com.aspose.words/txttrailingspacesoptions/) | Spécifie les options disponibles pour la gestion des espaces de fin lors de l'importation depuis le fichier [LoadFormat.\#TEXT](../com.aspose.words/loadformat/\#TEXT). |
| [Underline](../com.aspose.words/underline/) | Indique le type de soulignement appliqué à une police. |
| [UnicodeScript](../com.aspose.words/unicodescript/) | Propriété de la base de données Unicode : Script (sc). |
| [UnsupportedEncryptionException](../com.aspose.words/unsupportedencryptionexception/) | Levée lors du chargement du document, lorsque le document est chiffré avec une méthode non prise en charge. |
| [UnsupportedFileFormatException](../com.aspose.words/unsupportedfileformatexception/) | Levée lors du chargement du document, lorsque le format du document n'est pas reconnu ou n'est pas pris en charge par Aspose.Words. |
| [UserInformation](../com.aspose.words/userinformation/) | Spécifie les informations sur l'utilisateur. |
| [VariableCollection](../com.aspose.words/variablecollection/) | Une collection de variables de document. |
| [VariationAxis](../com.aspose.words/variationaxis/) | Représente le tag d'axe de variation de conception OpenType. |
| [VariationAxisCoordinate](../com.aspose.words/variationaxiscoordinate/) | Représente une coordonnée d'axe. |
| [VbaModule](../com.aspose.words/vbamodule/) | Fournit l'accès au module de projet VBA. |
| [VbaModuleCollection](../com.aspose.words/vbamodulecollection/) | Représente une collection d'objets [VbaModule](../com.aspose.words/vbamodule/). |
| [VbaModuleType](../com.aspose.words/vbamoduletype/) | Spécifie le type d'un modèle dans un projet VBA. |
| [VbaProject](../com.aspose.words/vbaproject/) | Fournit l'accès aux informations du projet VBA. |
| [VbaReference](../com.aspose.words/vbareference/) | Implémente une référence à une bibliothèque de types Automation ou à un projet VBA. |
| [VbaReferenceCollection](../com.aspose.words/vbareferencecollection/) | Représente une collection d'objets [VbaReference](../com.aspose.words/vbareference/). |
| [VbaReferenceType](../com.aspose.words/vbareferencetype/) | Permet de spécifier le type d'un objet [VbaReference](../com.aspose.words/vbareference/). |
| [VerticalAlignment](../com.aspose.words/verticalalignment/) | Spécifie l'alignement vertical d'une forme flottante, d'un cadre de texte ou d'un tableau flottant. |
| [ViewOptions](../com.aspose.words/viewoptions/) | Fournit diverses options qui contrôlent la façon dont un document est affiché dans Microsoft Word. |
| [ViewType](../com.aspose.words/viewtype/) | Valeurs possibles pour le mode d'affichage dans Microsoft Word. |
| [VisitorAction](../com.aspose.words/visitoraction/) | Permet au visiteur de contrôler l'énumération des nœuds. |
| [WarningInfo](../com.aspose.words/warninginfo/) | Contient des informations sur un avertissement émis par Aspose.Words lors du chargement ou de l'enregistrement du document. |
| [WarningInfoCollection](../com.aspose.words/warninginfocollection/) | Représente une collection typée d'objets [WarningInfo](../com.aspose.words/warninginfo/). |
| [WarningSource](../com.aspose.words/warningsource/) | Spécifie le module qui génère un avertissement lors du chargement ou de l'enregistrement du document. |
| [WarningType](../com.aspose.words/warningtype/) | Spécifie le type d'avertissement émis par Aspose.Words lors du chargement ou de l'enregistrement du document. |
| [Watermark](../com.aspose.words/watermark/) | Représente la classe permettant de travailler avec le filigrane du document. |
| [WatermarkLayout](../com.aspose.words/watermarklayout/) | Définit la disposition du filigrane par rapport au centre du filigrane. |
| [WatermarkType](../com.aspose.words/watermarktype/) | Spécifie le type de filigrane. |
| [Watermarker](../com.aspose.words/watermarker/) | Fournit des méthodes destinées à insérer des filigranes dans les documents. |
| [WatermarkerContext](../com.aspose.words/watermarkercontext/) | Contexte du filigraneur de document. |
| [WebExtension](../com.aspose.words/webextension/) | Représente un objet d'extension web. |
| [WebExtensionBinding](../com.aspose.words/webextensionbinding/) | Spécifie une relation de liaison entre une extension web et les données du document. |
| [WebExtensionBindingCollection](../com.aspose.words/webextensionbindingcollection/) | Spécifie une liste de liaisons d'extension web. |
| [WebExtensionBindingType](../com.aspose.words/webextensionbindingtype/) | Énumère les types disponibles de liaison entre une extension web et les données du document. |
| [WebExtensionProperty](../com.aspose.words/webextensionproperty/) | Spécifie une propriété personnalisée d'extension web. |
| [WebExtensionPropertyCollection](../com.aspose.words/webextensionpropertycollection/) | Spécifie un ensemble de propriétés personnalisées d'extension web. |
| [WebExtensionReference](../com.aspose.words/webextensionreference/) | Représente la référence à une extension web. |
| [WebExtensionReferenceCollection](../com.aspose.words/webextensionreferencecollection/) | Spécifie une liste de références d'extension web. |
| [WebExtensionStoreType](../com.aspose.words/webextensionstoretype/) | Énumère les types disponibles d'un magasin d'extension web. |
| [WordML2003SaveOptions](../com.aspose.words/wordml2003saveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#WORD\_ML](../com.aspose.words/saveformat/\#WORD-ML). |
| [WrapSide](../com.aspose.words/wrapside/) | Spécifie de quel(s) côté(s) de la forme ou de l'image le texte s'enroule. |
| [WrapType](../com.aspose.words/wraptype/) | Spécifie comment le texte s'enroule autour d'une forme ou d'une image. |
| [WriteProtection](../com.aspose.words/writeprotection/) | Spécifie les paramètres de protection en écriture pour un document. |
| [X509Certificate2Wrapper](../com.aspose.words/x509certificate2wrapper/) | Enveloppe publique ajoutée par JAVA autour de notre X509Certificate2 interne. |
| [XamlFixedSaveOptions](../com.aspose.words/xamlfixedsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#XAML\_FIXED](../com.aspose.words/saveformat/\#XAML-FIXED). |
| [XamlFlowSaveOptions](../com.aspose.words/xamlflowsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#XAML\_FLOW](../com.aspose.words/saveformat/\#XAML-FLOW) ou [SaveFormat.\#XAML\_FLOW\_PACK](../com.aspose.words/saveformat/\#XAML-FLOW-PACK). |
| [XlsxDateTimeParsingMode](../com.aspose.words/xlsxdatetimeparsingmode/) | Spécifie comment le texte du document est analysé pour identifier les valeurs de date et d'heure. |
| [XlsxSaveOptions](../com.aspose.words/xlsxsaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#XLSX](../com.aspose.words/saveformat/\#XLSX). |
| [XlsxSectionMode](../com.aspose.words/xlsxsectionmode/) | Spécifie comment les sections sont gérées lors de l'enregistrement d'un document au format XLSX. |
| [XmlDataLoadOptions](../com.aspose.words/xmldataloadoptions/) | Représente les options de chargement des données XML. |
| [XmlDataSource](../com.aspose.words/xmldatasource/) | Fournit l'accès aux données d'un fichier XML ou d'un flux à utiliser dans un rapport. |
| [XmlDsigLevel](../com.aspose.words/xmldsiglevel/) | Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig. |
| [XmlMapping](../com.aspose.words/xmlmapping/) | Spécifie les informations utilisées pour établir une correspondance entre la balise de document structuré parent et un élément XML stocké dans une partie de données XML personnalisée du document. |
| [XpsSaveOptions](../com.aspose.words/xpssaveoptions/) | Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document au format [SaveFormat.\#XPS](../com.aspose.words/saveformat/\#XPS). |
| [Zip64Mode](../com.aspose.words/zip64mode/) | Spécifie quand utiliser les extensions de format ZIP64 pour les fichiers OOXML. |
| [ZoomType](../com.aspose.words/zoomtype/) | Valeurs possibles pour la taille d'affichage du document à l'écran dans Microsoft Word. |

## Interfaces

| Interface | Description |
| --- | --- |
| [IBarcodeGenerator](../com.aspose.words/ibarcodegenerator/) | Interface publique pour le générateur personnalisé de codes-barres. |
| [IBibliographyStylesProvider](../com.aspose.words/ibibliographystylesprovider/) | Implémentez cette interface pour fournir le style bibliographique aux champs [FieldBibliography](../com.aspose.words/fieldbibliography/) et [FieldCitation](../com.aspose.words/fieldcitation/) lorsqu'ils sont mis à jour. |
| [IChartDataPoint](../com.aspose.words/ichartdatapoint/) | Contient les propriétés d'un seul point de données sur le graphique. |
| [IComparisonExpressionEvaluator](../com.aspose.words/icomparisonexpressionevaluator/) | Lorsqu'elle est implémentée, permet de remplacer l'évaluation des expressions de comparaison par défaut pour les champs [FieldIf](../com.aspose.words/fieldif/) et [FieldCompare](../com.aspose.words/fieldcompare/). |
| [ICssSavingCallback](../com.aspose.words/icsssavingcallback/) | Implémentez cette interface si vous souhaitez contrôler la façon dont Aspose.Words enregistre le CSS (Cascading Style Sheet) lors de l'enregistrement d'un document en HTML. |
| [IDocumentConverterPlugin](../com.aspose.words/idocumentconverterplugin/) | Définit une interface pour un plugin de convertisseur externe. |
| [IDocumentLoadingCallback](../com.aspose.words/idocumentloadingcallback/) | Implémentez cette interface si vous souhaitez disposer de votre propre méthode personnalisée appelée lors du chargement d'un document. |
| [IDocumentMergerPlugin](../com.aspose.words/idocumentmergerplugin/) | Définit une interface pour un plugin de fusion externe capable de fusionner des documents PDF. |
| [IDocumentPartSavingCallback](../com.aspose.words/idocumentpartsavingcallback/) | Implémentez cette interface si vous souhaitez recevoir des notifications et contrôler la façon dont Aspose.Words enregistre les parties du document lors de l'exportation d'un document au format [SaveFormat.\#HTML](../com.aspose.words/saveformat/\#HTML) ou [SaveFormat.\#EPUB](../com.aspose.words/saveformat/\#EPUB). |
| [IDocumentProcessorPlugin](../com.aspose.words/idocumentprocessorplugin/) | Définit une interface pour un plugin de traitement de documents externe. |
| [IDocumentReaderPlugin](../com.aspose.words/idocumentreaderplugin/) | Définit une interface pour des plugins de lecture externes capables de lire un fichier dans un document. |
| [IDocumentSavingCallback](../com.aspose.words/idocumentsavingcallback/) | Implémentez cette interface si vous souhaitez disposer de votre propre méthode personnalisée appelée lors de l'enregistrement d'un document. |
| [IFieldDatabaseProvider](../com.aspose.words/ifielddatabaseprovider/) | Implémentez cette interface pour fournir des données au champ [FieldDatabase](../com.aspose.words/fielddatabase/) lorsqu'il est mis à jour. |
| [IFieldMergingCallback](../com.aspose.words/ifieldmergingcallback/) | Implémentez cette interface si vous souhaitez contrôler la façon dont les données sont insérées dans les champs de fusion lors d'une opération de publipostage. |
| [IFieldResultFormatter](../com.aspose.words/ifieldresultformatter/) | Implémentez cette interface si vous souhaitez contrôler la façon dont le résultat du champ est formaté. |
| [IFieldUpdateCultureProvider](../com.aspose.words/ifieldupdatecultureprovider/) | Lorsqu'il est implémenté, fournit un objet [CultureInfo](../com.aspose.words.net.system.globalization/cultureinfo/) qui doit être utilisé lors de la mise à jour d'un champ particulier. |
| [IFieldUpdatingCallback](../com.aspose.words/ifieldupdatingcallback/) | Implémentez cette interface si vous souhaitez que vos propres méthodes personnalisées soient appelées pendant la mise à jour d'un champ. |
| [IFieldUpdatingProgressCallback](../com.aspose.words/ifieldupdatingprogresscallback/) | Implémentez cette interface si vous voulez suivre la progression de la mise à jour du champ. |
| [IFieldUserPromptRespondent](../com.aspose.words/ifielduserpromptrespondent/) | Représente le répondant aux invites de l'utilisateur pendant la mise à jour du champ. |
| [IFontSavingCallback](../com.aspose.words/ifontsavingcallback/) | Implémentez cette interface si vous souhaitez recevoir des notifications et contrôler la façon dont **Aspose.Words** enregistre les polices lors de l'exportation d'un document au format HTML. |
| [IHyphenationCallback](../com.aspose.words/ihyphenationcallback/) | Implémenté par des classes qui peuvent enregistrer des dictionnaires de césure. |
| [IImageSavingCallback](../com.aspose.words/iimagesavingcallback/) | Implémentez cette interface si vous souhaitez contrôler la façon dont **Aspose.Words** enregistre les images lors de l'enregistrement d'un document au format HTML. |
| [IIndexFilter](../com.aspose.words/iindexfilter/) | Définit un filtre pour ignorer les éléments en fonction de leurs indices. |
| [IMailMergeCallback](../com.aspose.words/imailmergecallback/) | Implémentez cette interface si vous souhaitez recevoir des notifications pendant l'exécution de la fusion de courrier. |
| [IMailMergeDataSource](../com.aspose.words/imailmergedatasource/) | Implémentez cette interface pour permettre la fusion de courrier à partir d'une source de données personnalisée, comme une liste d'objets. |
| [IMailMergeDataSourceRoot](../com.aspose.words/imailmergedatasourceroot/) | Implémentez cette interface pour permettre la fusion de courrier à partir d'une source de données personnalisée contenant des données maître-détail. |
| [INodeChangingCallback](../com.aspose.words/inodechangingcallback/) | Implémentez cette interface si vous souhaitez recevoir des notifications lorsque des nœuds sont insérés ou supprimés dans le document. |
| [IPageLayoutCallback](../com.aspose.words/ipagelayoutcallback/) | Implémentez cette interface si vous voulez que votre propre méthode personnalisée soit appelée pendant la construction et le rendu du modèle de mise en page. |
| [IPageSavingCallback](../com.aspose.words/ipagesavingcallback/) | Implémentez cette interface si vous souhaitez contrôler la façon dont **Aspose.Words** enregistre les pages séparées lors de l'enregistrement d'un document aux formats de page fixe. |
| [IReplacingCallback](../com.aspose.words/ireplacingcallback/) | Implémentez cette interface si vous voulez que votre propre méthode personnalisée soit appelée pendant une opération de recherche et remplacement. |
| [IResourceLoadingCallback](../com.aspose.words/iresourceloadingcallback/) | Implémentez cette interface si vous souhaitez contrôler la façon dont **Aspose.Words** charge les ressources externes lors de l'importation d'un document et de l'insertion d'images à l'aide de [DocumentBuilder](../com.aspose.words/documentbuilder/). |
| [IResourceSavingCallback](../com.aspose.words/iresourcesavingcallback/) | Implémentez cette interface si vous souhaitez contrôler la façon dont **Aspose.Words** enregistre les ressources externes (images, polices et CSS) lors de l'enregistrement d'un document au format HTML ou SVG à page fixe. |
| [IRevisionCriteria](../com.aspose.words/irevisioncriteria/) | Implémentez cette interface si vous souhaitez contrôler quand certaines [Revision](../com.aspose.words/revision/) doivent être acceptées/rejetées ou non par les méthodes [RevisionCollection.#accept(com.aspose.words.IRevisionCriteria)](../com.aspose.words/revisioncollection/#accept-com.aspose.words.IRevisionCriteria) / [RevisionCollection.#reject(com.aspose.words.IRevisionCriteria)](../com.aspose.words/revisioncollection/#reject-com.aspose.words.IRevisionCriteria). |
| [IStructuredDocumentTag](../com.aspose.words/istructureddocumenttag/) | Interface permettant de définir des données communes pour [StructuredDocumentTag](../com.aspose.words/structureddocumenttag/) et [StructuredDocumentTagRangeStart](../com.aspose.words/structureddocumenttagrangestart/). |
| [ITextShaper](../com.aspose.words/itextshaper/) | Fournit des méthodes pour la mise en forme du texte. |
| [ITextShaperFactory](../com.aspose.words/itextshaperfactory/) | Une interface d'une usine pour créer des implémentations de [ITextShaper](../com.aspose.words/itextshaper/). |
| [IWarningCallback](../com.aspose.words/iwarningcallback/) | Implémentez cette interface si vous souhaitez avoir votre propre méthode personnalisée appelée pour capturer les avertissements de perte de fidélité pouvant survenir lors du chargement ou de l'enregistrement d'un document. |
