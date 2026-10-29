---
title: Aspose::Words::Loading::LoadOptions class
linktitle: LoadOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions class. Allows to specify additional options (such as password or base URI) when loading a document into a Document object. To learn more, visit the Specify Load Options documentation article in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.loading/loadoptions/
---
## LoadOptions class


Allows to specify additional options (such as password or base URI) when loading a document into a [Document](../../aspose.words/document/) object. 
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) documentation article.

```cpp
class LoadOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [LoadOptions](./loadoptions/)() | Initializes a new instance of this class with default values. |
| [LoadOptions](./loadoptions/)(Aspose::Words::LoadFormat, const System::String \&, const System::String \&) | A shortcut to initialize a new instance of this class with properties set to the specified values. |
| [LoadOptions](./loadoptions/)(const System::String \&) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [get_BaseUri](./get_baseuri/)() const | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be **null** or empty string. Default is **null**. |
| [get_ConvertMetafilesToPng](./get_convertmetafilestopng/)() const | Gets or sets whether to convert metafile(**Wmf** or **Emf**) images to **Png** image format. |
| [get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/)() const | Gets or sets whether to convert shapes with EquationXML to Office Math objects. |
| [get_Encoding](./get_encoding/)() const | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be **null**. Default is **null**. |
| [get_FontSettings](./get_fontsettings/)() const | Allows to specify document font settings. |
| [get_IgnoreOleData](./get_ignoreoledata/)() const | Specifies whether to ignore the OLE data. |
| [get_LanguagePreferences](./get_languagepreferences/)() const | Gets language preferences that will be used when document is loading. |
| [get_LoadFormat](./get_loadformat/)() const | Specifies the format of the document to be loaded. Default is [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](./get_mswversion/)() const | Allows to specify that the document loading process should match a specific MS Word version. Default value is [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](./get_password/)() const | Gets or sets the password for opening an encrypted document. Can be **null** or empty string. Default is **null**. |
| [get_PreserveIncludePictureField](./get_preserveincludepicturefield/)() const | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | Called during loading a document and accepts data about loading progress. |
| [get_RecoveryMode](./get_recoverymode/)() const | Defines how the document should be handled if errors occur during loading. Use this property to specify whether the system should attempt to recover the document or follow another defined behavior. The default value is [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [get_TempFolder](./get_tempfolder/)() const | Allows to use temporary files when reading document. By default this property is **null** and no temporary files are used. |
| [get_UpdateDirtyFields](./get_updatedirtyfields/)() const | Specifies whether to update the fields with the **dirty** attribute. |
| [get_UseSystemLcid](./get_usesystemlcid/)() const | Gets or sets whether to use LCID value obtained from Windows registry to determine page setup default margins. |
| [get_WarningCallback](./get_warningcallback/)() const | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
| [set_BaseUri](./set_baseuri/)(const System::String \&) | Sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be **null** or empty string. Default is **null**. |
| [set_ConvertMetafilesToPng](./set_convertmetafilestopng/)(bool) | Sets whether to convert metafile(**Wmf** or **Emf**) images to **Png** image format. |
| [set_ConvertShapeToOfficeMath](./set_convertshapetoofficemath/)(bool) | Sets whether to convert shapes with EquationXML to Office Math objects. |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\> \&) | Sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be **null**. Default is **null**. |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\> \&) | Allows to specify document font settings. |
| [set_IgnoreOleData](./set_ignoreoledata/)(bool) | Specifies whether to ignore the OLE data. |
| [set_LoadFormat](./set_loadformat/)(Aspose::Words::LoadFormat) | Specifies the format of the document to be loaded. Default is [Auto](../../aspose.words/loadformat/). |
| [set_MswVersion](./set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Allows to specify that the document loading process should match a specific MS Word version. Default value is [Word2019](../../aspose.words.settings/mswordversion/) |
| [set_Password](./set_password/)(const System::String \&) | Sets the password for opening an encrypted document. Can be **null** or empty string. Default is **null**. |
| [set_PreserveIncludePictureField](./set_preserveincludepicturefield/)(bool) | Sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is **false**. |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\> \&) | Called during loading a document and accepts data about loading progress. |
| [set_RecoveryMode](./set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Defines how the document should be handled if errors occur during loading. Use this property to specify whether the system should attempt to recover the document or follow another defined behavior. The default value is [TryRecover](../documentrecoverymode/). |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\> \&) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [set_TempFolder](./set_tempfolder/)(const System::String \&) | Allows to use temporary files when reading document. By default this property is **null** and no temporary files are used. |
| [set_UpdateDirtyFields](./set_updatedirtyfields/)(bool) | Specifies whether to update the fields with the **dirty** attribute. |
| [set_UseSystemLcid](./set_usesystemlcid/)(bool) | Sets whether to use LCID value obtained from Windows registry to determine page setup default margins. |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\> \&) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
## Examples


Shows how to load an encrypted Microsoft Word document.

```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words throw an exception if we try to open an encrypted document without its password.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Encrypted.docx"));
})(), Aspose::Words::IncorrectPasswordException);

// When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// There are two ways of loading an encrypted document with a LoadOptions object.
// 1 -  Load the document from the local file system by filename:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Load the document from a stream:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```
## See Also

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
