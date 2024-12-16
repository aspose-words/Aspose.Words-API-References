---
title: Aspose::Words::Loading::TxtLoadOptions class
linktitle: TxtLoadOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::TxtLoadOptions class. Allows to specify additional options when loading Text document into a Document object. To learn more, visit the  documentation article in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class


Allows to specify additional options when loading [Text](../../aspose.words/loadformat/) document into a [Document](../../aspose.words/document/) object. To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) documentation article.

```cpp
class TxtLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Methods

| Method | Description |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [get_AutoNumberingDetection](./get_autonumberingdetection/)() const | Gets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is **true**. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be **null** or empty string. Default is **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Gets or sets whether to convert metafile([Wmf](../) or [Emf](../)) images to [Png](../) image format. |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Gets or sets whether to convert shapes with EquationXML to Office [Math](../../aspose.words.math/) objects. |
| [get_DetectHyperlinks](./get_detecthyperlinks/)() const | Specifies either to detect hyperlinks in text. The default value is **false**. |
| [get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/)() const | Allows to specify how numbered list items are recognized when document is imported from plain text format. The default value is **true**. |
| [get_DocumentDirection](./get_documentdirection/)() const | Gets or sets a document direction. The default value is [LeftToRight](../documentdirection/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be **null**. Default is **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Allows to specify document font settings. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Specifies whether to ignore the OLE data. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Gets language preferences that will be used when document is loading. |
| [get_LeadingSpacesOptions](./get_leadingspacesoptions/)() const | Gets or sets preferred option of a leading space handling. Default value is [ConvertToIndent](../txtleadingspacesoptions/). |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Specifies the format of the document to be loaded. Default is [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Allows to specify that the document loading process should match a specific MS Word version. Default value is [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Gets or sets the password for opening an encrypted document. Can be **null** or empty string. Default is **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Called during loading a document and accepts data about loading progress. |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Allows to use temporary files when reading document. By default this property is **null** and no temporary files are used. |
| [get_TrailingSpacesOptions](./get_trailingspacesoptions/)() const | Gets or sets preferred option of a trailing space handling. Default value is [Trim](../txttrailingspacesoptions/). |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Specifies whether to update the fields with the **dirty** attribute. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Initializes a new instance of this class with default values. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | A shortcut to initialize a new instance of this class with properties set to the specified values. |
| [set_AutoNumberingDetection](./set_autonumberingdetection/)(bool) | Sets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is **true**. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_DetectHyperlinks](./set_detecthyperlinks/)(bool) | Specifies either to detect hyperlinks in text. The default value is **false**. |
| [set_DetectNumberingWithWhitespaces](./set_detectnumberingwithwhitespaces/)(bool) | Setter for [Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/). |
| [set_DocumentDirection](./set_documentdirection/)(Aspose::Words::Loading::DocumentDirection) | Setter for [Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection](./get_documentdirection/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LeadingSpacesOptions](./set_leadingspacesoptions/)(Aspose::Words::Loading::TxtLeadingSpacesOptions) | Setter for [Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions](./get_leadingspacesoptions/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Setter for [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Setter for [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Called during loading a document and accepts data about loading progress. |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/). |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_TrailingSpacesOptions](./set_trailingspacesoptions/)(Aspose::Words::Loading::TxtTrailingSpacesOptions) | Setter for [Aspose::Words::Loading::TxtLoadOptions::get_TrailingSpacesOptions](./get_trailingspacesoptions/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Specifies whether to update the fields with the **dirty** attribute. |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_WarningCallback](../loadoptions/get_warningcallback/). |
| [TxtLoadOptions](./txtloadoptions/)() | Initializes a new instance of this class with default values. |
| static [Type](./type/)() |  |
## See Also

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
