---
title: Aspose::Words::Loading::RtfLoadOptions class
linktitle: RtfLoadOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::RtfLoadOptions class. Allows to specify additional options when loading Rtf document into a Document object. To learn more, visit the  documentation article in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.loading/rtfloadoptions/
---
## RtfLoadOptions class


Allows to specify additional options when loading [Rtf](../../aspose.words/loadformat/) document into a [Document](../../aspose.words/document/) object. To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) documentation article.

```cpp
class RtfLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Methods

| Method | Description |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be **null** or empty string. Default is **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Gets or sets whether to convert metafile([Wmf](../) or [Emf](../)) images to [Png](../) image format. |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Gets or sets whether to convert shapes with EquationXML to Office [Math](../../aspose.words.math/) objects. |
| [get_Encoding](../loadoptions/get_encoding/)() const | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be **null**. Default is **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Allows to specify document font settings. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Specifies whether to ignore the OLE data. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Gets language preferences that will be used when document is loading. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Specifies the format of the document to be loaded. Default is [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Allows to specify that the document loading process should match a specific MS Word version. Default value is [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Gets or sets the password for opening an encrypted document. Can be **null** or empty string. Default is **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Called during loading a document and accepts data about loading progress. |
| [get_RecognizeUtf8Text](./get_recognizeutf8text/)() const | When set to **true**, will try to detect UTF8 characters, they will be preserved during import. |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Allows to use temporary files when reading document. By default this property is **null** and no temporary files are used. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Specifies whether to update the fields with the **dirty** attribute. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Initializes a new instance of this class with default values. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | A shortcut to initialize a new instance of this class with properties set to the specified values. |
| [RtfLoadOptions](./rtfloadoptions/)() | Initializes a new instance of this class with default values. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Setter for [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Setter for [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Called during loading a document and accepts data about loading progress. |
| [set_RecognizeUtf8Text](./set_recognizeutf8text/)(bool) | Setter for [Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text](./get_recognizeutf8text/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
| static [Type](./type/)() |  |

## Examples



Shows how to detect UTF-8 characters while loading an RTF document. 
```cpp
// Create an "RtfLoadOptions" object to modify how we load an RTF document.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// Set the "RecognizeUtf8Text" property to "false" to assume that the document uses the ISO 8859-1 charset
// and loads every character in the document.
// Set the "RecognizeUtf8Text" property to "true" to parse any variable-length characters that may occur in the text.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## See Also

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
