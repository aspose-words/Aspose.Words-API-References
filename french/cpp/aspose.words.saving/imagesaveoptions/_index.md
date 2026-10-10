---
title: "Aspose::Words::Saving::ImageSaveOptions class"
linktitle: "ImageSaveOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSaveOptions class. Permet de spécifier des options supplémentaires lors du rendu des pages de document ou des formes en images. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class


Permet de spécifier des options supplémentaires lors du rendu des pages ou des formes du document en images. Pour en savoir plus, consultez l'article de documentation [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class ImageSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clone](./clone/)() | Crée une copie profonde de cet objet. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Crée un objet d'options d'enregistrement d'une classe adaptée au format d'enregistrement spécifié. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Crée un objet d'options d'enregistrement d'une classe adaptée à l'extension de fichier spécifiée dans le nom de fichier fourni. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Obtient une valeur déterminant la façon dont les couleurs sont rendues. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs date/heure. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Obtient ou définit le chemin vers le modèle par défaut (y compris le nom de fichier). La valeur par défaut pour cette propriété est **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Obtient une valeur déterminant comment les effets 3D sont rendus. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Obtient ou définit une valeur déterminant comment les effets DrawingML sont rendus. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les formes DrawingML sont rendues. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Lorsque **true**, le nom et la version d'Aspose.Words sont incorporés dans les fichiers produits. La valeur par défaut est **true**. |
| [get_GraphicsQualityOptions](./get_graphicsqualityoptions/)() const | Permet de spécifier le mode de rendu et la qualité pour l'objet **Graphics**. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Obtient ou définit la résolution horizontale des images générées, en points par pouce. |
| [get_ImageBrightness](./get_imagebrightness/)() const | Obtient ou définit la luminosité des images générées. |
| [get_ImageColorMode](./get_imagecolormode/)() const | Obtient ou définit le mode couleur des images générées. |
| [get_ImageContrast](./get_imagecontrast/)() const | Obtient ou définit le contraste des images générées. |
| [get_ImageSize](./get_imagesize/)() const | Obtient ou définit la taille d'une image générée en pixels. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Obtient ou définit une valeur déterminant comment les objets encre (InkML) sont rendus. |
| [get_JpegQuality](./get_jpegquality/)() | Obtient ou définit une valeur déterminant la qualité des images JPEG générées. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document Html. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Obtient la valeur déterminant si l’optimisation de la mémoire doit être effectuée avant d’enregistrer le document. La valeur par défaut pour cette propriété est **false**. |
| [get_MetafileRenderingOptions](./get_metafilerenderingoptions/)() | Permet de spécifier comment les métafichiers sont traités dans la sortie rendue. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Permet de spécifier les options de rendu des métafichiers. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Obtient le [NumeralFormat](../numeralformat/) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Le drapeau indique s'il est nécessaire d'optimiser la sortie. Si ce drapeau est activé, les canevas imbriqués redondants et les canevas vides sont supprimés, de même que les glyphes voisins ayant le même formatage sont concaténés. Remarque : la précision de l'affichage du contenu peut être affectée si cette propriété est définie sur **true**. La valeur par défaut est **false**. |
| [get_PageLayout](./get_pagelayout/)() const | Obtient ou définit la disposition utilisée lors du rendu de plusieurs pages en une seule sortie. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Permet de contrôler la façon dont les pages séparées sont enregistrées lorsqu'un document est exporté au format page fixe. |
| [get_PageSet](./get_pageset/)() | Obtient ou définit les pages à rendre. La valeur par défaut est toutes les pages du document. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Obtient ou définit les pages à rendre. La valeur par défaut est toutes les pages du document. |
| [get_PaperColor](./get_papercolor/)() | Obtient ou définit la couleur d'arrière-plan (papier) des images générées. La valeur par défaut est **White**. |
| [get_PixelFormat](./get_pixelformat/)() const | Obtient ou définit le format de pixel des images générées. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Lorsque **true**, le formatage « pretty » est appliqué à la sortie lorsque c’est possible. La valeur par défaut est **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Appelé lors de l’enregistrement d’un document et accepte les données concernant la progression de l’enregistrement. |
| [get_SaveFormat](./get_saveformat/)() override | Spécifie le format dans lequel les pages de document ou les formes rendues seront enregistrées si cet objet d'options d'enregistrement est utilisé. Peut être un raster [Tiff](../../aspose.words/saveformat/), [Png](../../aspose.words/saveformat/), [Bmp](../../aspose.words/saveformat/), [Jpeg](../../aspose.words/saveformat/) ou un vecteur [Emf](../../aspose.words/saveformat/), [Eps](../../aspose.words/saveformat/), [WebP](../), [Svg](../../aspose.words/saveformat/). |
| [get_Scale](./get_scale/)() const | Obtient ou définit le facteur de zoom des images générées. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement en fichier DOC ou DOCX. Par défaut, cette propriété est **null** et aucun fichier temporaire n'est utilisé. |
| [get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/)() const | Obtient ou définit le seuil qui détermine la valeur de l'erreur de binarisation dans la méthode Floyd‑Steinberg lorsque [ImageBinarizationMethod](../imagebinarizationmethod/) est [FloydSteinbergDithering](../imagebinarizationmethod/). |
| [get_TiffBinarizationMethod](./get_tiffbinarizationmethod/)() const | Obtient ou définit la méthode utilisée lors de la conversion des images au format 1 bpp lorsque [SaveFormat](./get_saveformat/) est [Tiff](../../aspose.words/saveformat/) et que [TiffCompression](./get_tiffcompression/) est égal à [Ccitt3](../tiffcompression/) ou [Ccitt4](../tiffcompression/). |
| [get_TiffCompression](./get_tiffcompression/)() const | Obtient ou définit le type de compression à appliquer lors de l'enregistrement des images générées au format TIFF. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) est mise à jour avant l'enregistrement. La valeur par défaut est **false** ; |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Obtient une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut pour cette propriété est **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) est mise à jour avant l'enregistrement. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Obtient ou définit une valeur déterminant si la propriété [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) est mise à jour avant l'enregistrement. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Obtient une valeur déterminant si l'image de présentation des contrôles OLE sera mise à jour. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage lors du rendu. |
| [get_UseGdiEmfRenderer](./get_usegdiemfrenderer/)() const | Obtient ou définit une valeur déterminant s'il faut utiliser le rendu GDI+ ou le rendu de métafichier Aspose.Words lors de l'enregistrement au format EMF. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c’est‑à‑dire lents). |
| [get_VerticalResolution](./get_verticalresolution/)() const | Obtient ou définit la résolution verticale des images générées, en points par pouce. |
| [GetType](./gettype/)() const override |  |
| [ImageSaveOptions](./imagesaveoptions/)(Aspose::Words::SaveFormat) | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer les images rendues aux formats [Tiff](../../aspose.words/saveformat/), [Png](../../aspose.words/saveformat/), [Bmp](../../aspose.words/saveformat/), [Jpeg](../../aspose.words/saveformat/), [Emf](../../aspose.words/saveformat/), [Eps](../../aspose.words/saveformat/), [WebP](../) ou [Svg](../../aspose.words/saveformat/). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Définit une valeur déterminant comment les couleurs sont rendues. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Mutateur pour [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Définit une valeur déterminant comment les effets 3D sont rendus. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_GraphicsQualityOptions](./set_graphicsqualityoptions/)(const System::SharedPtr\<Aspose::Words::Saving::GraphicsQualityOptions\>\&) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_GraphicsQualityOptions](./get_graphicsqualityoptions/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(float) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_ImageBrightness](./set_imagebrightness/)(float) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness](./get_imagebrightness/). |
| [set_ImageColorMode](./set_imagecolormode/)(Aspose::Words::Saving::ImageColorMode) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_ImageColorMode](./get_imagecolormode/). |
| [set_ImageContrast](./set_imagecontrast/)(float) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast](./get_imagecontrast/). |
| [set_ImageSize](./set_imagesize/)(System::Drawing::Size) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_ImageSize](./get_imagesize/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Permet de spécifier les options de rendu des métafichiers. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Définit [NumeralFormat](../numeralformat/) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Mutateur pour [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageLayout](./set_pagelayout/)(const System::SharedPtr\<Aspose::Words::Saving::MultiPageLayout\>\&) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_PageLayout](./get_pagelayout/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Permet de contrôler la façon dont les pages séparées sont enregistrées lorsqu'un document est exporté au format page fixe. |
| [set_PageSet](./set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_PageSet](./get_pageset/). |
| [set_PaperColor](./set_papercolor/)(System::Drawing::Color) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_PaperColor](./get_papercolor/). |
| [set_PixelFormat](./set_pixelformat/)(Aspose::Words::Saving::ImagePixelFormat) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_PixelFormat](./get_pixelformat/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_Resolution](./set_resolution/)(float) | Définit à la fois la résolution horizontale et verticale des images générées, en points par pouce. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_Scale](./set_scale/)(float) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_Scale](./get_scale/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_ThresholdForFloydSteinbergDithering](./set_thresholdforfloydsteinbergdithering/)(uint8_t) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/). |
| [set_TiffBinarizationMethod](./set_tiffbinarizationmethod/)(Aspose::Words::Saving::ImageBinarizationMethod) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod](./get_tiffbinarizationmethod/). |
| [set_TiffCompression](./set_tiffcompression/)(Aspose::Words::Saving::TiffCompression) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_TiffCompression](./get_tiffcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Définisseur de [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Définit une valeur déterminant si l'image de présentation des contrôles OLE sera mise à jour. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseGdiEmfRenderer](./set_usegdiemfrenderer/)(bool) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer](./get_usegdiemfrenderer/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Définisseur pour [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_VerticalResolution](./set_verticalresolution/)(float) | Définisseur de [Aspose::Words::Saving::ImageSaveOptions::get_VerticalResolution](./get_verticalresolution/). |
| static [Type](./type/)() |  |

## Exemples



Rend une page d'un document Word en image avec un arrière-plan transparent ou coloré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Définissez la propriété "PaperColor" sur une couleur transparente pour appliquer une transparente
// arrière-plan au document lors du rendu en image.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Définissez la propriété "PaperColor" sur une couleur opaque pour appliquer cette couleur
// comme arrière-plan du document lors du rendu en image.
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```


Montre comment configurer la compression lors de l'enregistrement d'un document au format JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Définissez la propriété "JpegQuality" sur "10" pour utiliser une compression plus forte lors du rendu du document.
// Cela réduira la taille du fichier du document, mais l'image affichera des artefacts de compression plus visibles.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Définissez la propriété "JpegQuality" sur "100" pour utiliser une compression plus faible lors du rendu du document.
// Cela améliorera la qualité de l'image au prix d'une taille de fichier accrue.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```


Montre comment spécifier une résolution lors du rendu d'un document au format PNG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
// pour modifier la façon dont cette méthode rend le document en image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Définissez la propriété "Resolution" sur "72" pour rendre le document à 72 dpi.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// Définissez la propriété "Resolution" sur "300" pour rendre le document à 300 dpi.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## Voir aussi

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
