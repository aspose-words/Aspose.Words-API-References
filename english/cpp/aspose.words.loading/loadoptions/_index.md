---
title: LoadOptions
second_title: Aspose.Words for C++ API Reference
description: Allows to specify additional options (such as password or base URI) when loading a document into a Document object. To learn more, visit the  documentation article.
type: docs
weight: 53
url: /cpp/aspose.words.loading/loadoptions/
---
## LoadOptions class


Allows to specify additional options (such as password or base URI) when loading a document into a [Document](../../aspose.words/document/) object. To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) documentation article.

```cpp
class LoadOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_BaseUri](./get_baseuri/)() const | Gets or sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be null or empty string. Default is null. |
| [get_ConvertMetafilesToPng](./get_convertmetafilestopng/)() const | Gets or sets whether to convert metafile ([Wmf](../) or [Emf](../)) images to [Png](../) image format. |
| [get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/)() const | Gets or sets whether to convert shapes with EquationXML to Office [Math](../../aspose.words.math/) objects. |
| [get_Encoding](./get_encoding/)() const | Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be null. Default is null. |
| [get_FontSettings](./get_fontsettings/)() const | Allows to specify document font settings. |
| [get_LanguagePreferences](./get_languagepreferences/)() const | Gets language preferences that will be used when document is loading. |
| [get_LoadFormat](./get_loadformat/)() const | Specifies the format of the document to be loaded. Default is [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](./get_mswversion/)() const | Allows to specify that the document loading process should match a specific MS Word version. Default value is [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](./get_password/)() const | Gets or sets the password for opening an encrypted document. Can be null or empty string. Default is null. |
| [get_PreserveIncludePictureField](./get_preserveincludepicturefield/)() const | Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is false. |
| [get_ProgressCallback](./get_progresscallback/)() const | Called during loading a document and accepts data about loading progress. |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [get_TempFolder](./get_tempfolder/)() const | Allows to use temporary files when reading document. By default this property is **null** and no temporary files are used. |
| [get_UpdateDirtyFields](./get_updatedirtyfields/)() const | Specifies whether to update the fields with the **dirty** attribute. |
| [get_WarningCallback](./get_warningcallback/)() const | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
| [LoadOptions](./loadoptions/)() | Initializes a new instance of this class with default values. |
| [LoadOptions](./loadoptions/)(const System::String\&) | A shortcut to initialize a new instance of this class with the specified password to load an encrypted document. |
| [LoadOptions](./loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | A shortcut to initialize a new instance of this class with properties set to the specified values. |
| [set_BaseUri](./set_baseuri/)(const System::String\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_BaseUri](./get_baseuri/). |
| [set_ConvertMetafilesToPng](./set_convertmetafilestopng/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](./get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](./set_convertshapetoofficemath/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_Encoding](./get_encoding/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_FontSettings](./get_fontsettings/). |
| [set_LoadFormat](./set_loadformat/)(Aspose::Words::LoadFormat) | Setter for [Aspose::Words::Loading::LoadOptions::get_LoadFormat](./get_loadformat/). |
| [set_MswVersion](./set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Setter for [Aspose::Words::Loading::LoadOptions::get_MswVersion](./get_mswversion/). |
| [set_Password](./set_password/)(const System::String\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_Password](./get_password/). |
| [set_PreserveIncludePictureField](./set_preserveincludepicturefield/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](./get_preserveincludepicturefield/). |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Called during loading a document and accepts data about loading progress. |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_ResourceLoadingCallback](./get_resourceloadingcallback/). |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateDirtyFields](./set_updatedirtyfields/)(bool) | Setter for [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](./get_updatedirtyfields/). |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Setter for [Aspose::Words::Loading::LoadOptions::get_WarningCallback](./get_warningcallback/). |

## Examples



Shows how to load an encrypted Microsoft Word document. 
```cpp
SharedPtr<Document> doc;

// Aspose.Words throw an exception if we try to open an encrypted document without its password.
ASSERT_THROW(doc = MakeObject<Document>(MyDir + u"Encrypted.docx"), IncorrectPasswordException);

// When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
auto options = MakeObject<LoadOptions>(u"docPassword");

// There are two ways of loading an encrypted document with a LoadOptions object.
// 1 -  Load the document from the local file system by filename:
doc = MakeObject<Document>(MyDir + u"Encrypted.docx", options);

// 2 -  Load the document from a stream:
{
    SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(MyDir + u"Encrypted.docx");
    doc = MakeObject<Document>(stream, options);
}
```

## See Also

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words](../../)
