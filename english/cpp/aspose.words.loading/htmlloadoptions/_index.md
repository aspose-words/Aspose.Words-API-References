---
title: Aspose::Words::Loading::HtmlLoadOptions class
linktitle: HtmlLoadOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::HtmlLoadOptions class. Allows to specify additional options when loading HTML document into a Document object. To learn more, visit the Specify Load Options documentation article in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class


Allows to specify additional options when loading HTML document into a [Document](../../aspose.words/document/) object. 
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) documentation article.

```cpp
class HtmlLoadOptions : public LoadOptions
```

## Methods

| Method | Description |
| --- | --- |
| [HtmlLoadOptions](./htmlloadoptions/)() | Initializes a new instance of this class with default values. |
| [HtmlLoadOptions](./htmlloadoptions/)(Aspose::Words::LoadFormat, const System::String \&, const System::String \&) | A shortcut to initialize a new instance of this class with properties set to the specified values. |
| [HtmlLoadOptions](./htmlloadoptions/)(const System::String \&) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [get_BlockImportMode](./get_blockimportmode/)() const | Gets or sets a value that specifies how properties of block-level elements are imported. Default value is [Merge](../blockimportmode/). |
| [get_ConvertSvgToEmf](./get_convertsvgtoemf/)() const | Gets or sets a value indicating whether to convert loaded SVG images to the EMF format. Default value is **false** and, if possible, loaded SVG images are stored as is without conversion. |
| [get_IgnoreNoscriptElements](./get_ignorenoscriptelements/)() const | Gets or sets a value indicating whether to ignore <noscript> HTML elements. Default value is **false**. |
| [get_PreferredControlType](./get_preferredcontroltype/)() const | Gets or sets preferred type of document nodes that will represent imported <input> and <select> elements. Default value is [FormField](../htmlcontroltype/). |
| [get_SupportFontFaceRules](./get_supportfontfacerules/)() const | Gets or sets a value indicating whether to support @font-face rules and whether to load declared fonts. Default value is **false**. |
| [get_SupportVml](./get_supportvml/)() const | Gets or sets a value indicating whether to support VML images. |
| [get_WebRequestTimeout](./get_webrequesttimeout/)() const | The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds (100 seconds). |
| [set_BlockImportMode](./set_blockimportmode/)(Aspose::Words::Loading::BlockImportMode) | Sets a value that specifies how properties of block-level elements are imported. Default value is [Merge](../blockimportmode/). |
| [set_ConvertSvgToEmf](./set_convertsvgtoemf/)(bool) | Sets a value indicating whether to convert loaded SVG images to the EMF format. Default value is **false** and, if possible, loaded SVG images are stored as is without conversion. |
| [set_IgnoreNoscriptElements](./set_ignorenoscriptelements/)(bool) | Sets a value indicating whether to ignore <noscript> HTML elements. Default value is **false**. |
| [set_PreferredControlType](./set_preferredcontroltype/)(Aspose::Words::Loading::HtmlControlType) | Sets preferred type of document nodes that will represent imported <input> and <select> elements. Default value is [FormField](../htmlcontroltype/). |
| [set_SupportFontFaceRules](./set_supportfontfacerules/)(bool) | Sets a value indicating whether to support @font-face rules and whether to load declared fonts. Default value is **false**. |
| [set_SupportVml](./set_supportvml/)(bool) | Sets a value indicating whether to support VML images. |
| [set_WebRequestTimeout](./set_webrequesttimeout/)(int32_t) | The number of milliseconds to wait before the web request times out. The default value is 100000 milliseconds (100 seconds). |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [LoadOptions](../loadoptions/loadoptions/)() | Initializes a new instance of this class with default values. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String \&, const System::String \&) | A shortcut to initialize a new instance of this class with properties set to the specified values. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String \&) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be **null** or empty string. Default is **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Gets or sets whether to convert metafile(**Wmf** or **Emf**) images to **Png** image format. |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Gets or sets whether to convert shapes with EquationXML to Office Math objects. |
| [get_Encoding](../loadoptions/get_encoding/)() const | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be **null**. Default is **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Allows to specify document font settings. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Specifies whether to ignore the OLE data. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Gets language preferences that will be used when document is loading. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Specifies the format of the document to be loaded. Default is [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Allows to specify that the document loading process should match a specific MS Word version. Default value is [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Gets or sets the password for opening an encrypted document. Can be **null** or empty string. Default is **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Called during loading a document and accepts data about loading progress. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Defines how the document should be handled if errors occur during loading. Use this property to specify whether the system should attempt to recover the document or follow another defined behavior. The default value is [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Allows to use temporary files when reading document. By default this property is **null** and no temporary files are used. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Specifies whether to update the fields with the **dirty** attribute. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String \&) | Sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be **null** or empty string. Default is **null**. |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Sets whether to convert metafile(**Wmf** or **Emf**) images to **Png** image format. |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Sets whether to convert shapes with EquationXML to Office Math objects. |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\> \&) | Sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be **null**. Default is **null**. |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\> \&) | Allows to specify document font settings. |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Specifies whether to ignore the OLE data. |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Specifies the format of the document to be loaded. Default is [Auto](../../aspose.words/loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [Word2019](../../aspose.words.settings/mswordversion/) |
| [set_Password](../loadoptions/set_password/)(const System::String \&) | Sets the password for opening an encrypted document. Can be **null** or empty string. Default is **null**. |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is **false**. |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\> \&) | Called during loading a document and accepts data about loading progress. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Defines how the document should be handled if errors occur during loading. Use this property to specify whether the system should attempt to recover the document or follow another defined behavior. The default value is [TryRecover](../documentrecoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\> \&) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String \&) | Allows to use temporary files when reading document. By default this property is **null** and no temporary files are used. |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Specifies whether to update the fields with the **dirty** attribute. |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Sets whether to use LCID value obtained from Windows registry to determine page setup default margins. |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\> \&) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
## Examples


Shows how to support conditional comments while loading an HTML document.

```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// If the value is true, then we take VML code into account while parsing the loaded document.
loadOptions->set_SupportVml(supportVml);

// This document contains a JPEG image within "<!--[if gte vml 1]>" tags,
// and a different PNG image within "<![if !vml]>" tags.
// If we set the "SupportVml" flag to "true", then Aspose.Words will load the JPEG.
// If we set this flag to "false", then Aspose.Words will only load the PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```
## See Also

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
