---
title: Aspose::Words::Loading::TxtLoadOptions class
linktitle: TxtLoadOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::TxtLoadOptions class. Allows to specify additional options when loading Text document into a Document object. To learn more, visit the Specify Load Options documentation article in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class


Allows to specify additional options when loading [Text](../../aspose.words/loadformat/) document into a [Document](../../aspose.words/document/) object. 
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) documentation article.

```cpp
class TxtLoadOptions : public LoadOptions
```

## Methods

| Method | Description |
| --- | --- |
| [TxtLoadOptions](./txtloadoptions/)() | Initializes a new instance of this class with default values. |
| [get_AutoNumberingDetection](./get_autonumberingdetection/)() const | Gets or sets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is **true**. |
| [get_DetectHyperlinks](./get_detecthyperlinks/)() const | Specifies either to detect hyperlinks in text. The default value is **false**. |
| [get_DetectNumberingWithWhitespaces](./get_detectnumberingwithwhitespaces/)() const | Allows to specify how numbered list items are recognized when document is imported from plain text format. The default value is **true**. |
| [get_DocumentDirection](./get_documentdirection/)() const | Gets or sets a document direction. The default value is [LeftToRight](../documentdirection/). |
| [get_LeadingSpacesOptions](./get_leadingspacesoptions/)() const | Gets or sets preferred option of a leading space handling. Default value is [ConvertToIndent](../txtleadingspacesoptions/). |
| [get_TrailingSpacesOptions](./get_trailingspacesoptions/)() const | Gets or sets preferred option of a trailing space handling. Default value is [Trim](../txttrailingspacesoptions/). |
| [set_AutoNumberingDetection](./set_autonumberingdetection/)(bool) | Sets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is **true**. |
| [set_DetectHyperlinks](./set_detecthyperlinks/)(bool) | Specifies either to detect hyperlinks in text. The default value is **false**. |
| [set_DetectNumberingWithWhitespaces](./set_detectnumberingwithwhitespaces/)(bool) | Allows to specify how numbered list items are recognized when document is imported from plain text format. The default value is **true**. |
| [set_DocumentDirection](./set_documentdirection/)(Aspose::Words::Loading::DocumentDirection) | Sets a document direction. The default value is [LeftToRight](../documentdirection/). |
| [set_LeadingSpacesOptions](./set_leadingspacesoptions/)(Aspose::Words::Loading::TxtLeadingSpacesOptions) | Sets preferred option of a leading space handling. Default value is [ConvertToIndent](../txtleadingspacesoptions/). |
| [set_TrailingSpacesOptions](./set_trailingspacesoptions/)(Aspose::Words::Loading::TxtTrailingSpacesOptions) | Sets preferred option of a trailing space handling. Default value is [Trim](../txttrailingspacesoptions/). |
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


Shows how to read and display hyperlinks.

```cpp
const System::String inputText = System::String(u"Some links in TXT:\n") + u"https://www.aspose.com/\n" + u"https://docs.aspose.com/words/net/\n";

{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::MemoryStream>();
    System::ArrayPtr<uint8_t> buf = System::Text::Encoding::get_ASCII()->GetBytes(inputText);
    stream->Write(buf, 0, buf->get_Length());
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();
    loadOptions->set_DetectHyperlinks(true);

    // Load document with hyperlinks.
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Print hyperlinks text.
    for (auto&& field : System::IterateOver(doc->get_Range()->get_Fields()))
    {
        std::cout << field->get_Result() << std::endl;
    }

    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(0)->get_Result().Trim(), u"https://www.aspose.com/");
    ASSERT_EQ(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().Trim(), u"https://docs.aspose.com/words/net/");
}
```
## See Also

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
