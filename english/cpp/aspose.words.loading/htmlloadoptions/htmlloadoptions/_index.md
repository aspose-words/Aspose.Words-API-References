---
title: HtmlLoadOptions
second_title: Aspose.Words for C++ API Reference
description: Initializes a new instance of this class with default values.
type: docs
weight: 1
url: /cpp/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions::HtmlLoadOptions() constructor


Initializes a new instance of this class with default values.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions()
```


## Examples



Shows how to support conditional comments while loading an HTML document. 
```cpp
auto loadOptions = MakeObject<HtmlLoadOptions>();

// If the value is true, then we take VML code into account while parsing the loaded document.
loadOptions->set_SupportVml(supportVml);

// This document contains a JPEG image within "<!--[if gte vml 1]>" tags,
// and a different PNG image within "<![if !vml]>" tags.
// If we set the "SupportVml" flag to "true", then Aspose.Words will load the JPEG.
// If we set this flag to "false", then Aspose.Words will only load the PNG.
auto doc = MakeObject<Document>(MyDir + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(ImageType::Jpeg, (System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(ImageType::Png, (System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## See Also

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
## HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


A shortcut to initialize a new instance of this class with properties set to the specified values.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
```


| Parameter | Type | Description |
| --- | --- | --- |
| loadFormat | Aspose::Words::LoadFormat | The format of the document to be loaded. |
| password | const System::String\& | The password to open an encrypted document. Can be null or empty string. |
| baseUri | const System::String\& | The string that will be used to resolve relative URIs to absolute. Can be null or empty string. |

## Examples



Shows how to specify a base URI when opening an html document. 
```cpp
// Suppose we want to load an .html document that contains an image linked by a relative URI
// while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
// We can provide a base URI using an HtmlLoadOptions object.
auto loadOptions = MakeObject<HtmlLoadOptions>(LoadFormat::Html, u"", ImageDir);

ASSERT_EQ(LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = MakeObject<Document>(MyDir + u"Missing image.html", loadOptions);

// While the image was broken in the input .html, our custom base URI helped us repair the link.
auto imageShape = System::DynamicCast<Shape>(doc->GetChildNodes(NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// This output document will display the image that was missing.
doc->Save(ArtifactsDir + u"HtmlLoadOptions.BaseUri.docx");
```

## See Also

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
## HtmlLoadOptions::HtmlLoadOptions(const System::String\&) constructor


A shortcut to initialize a new instance of this class with the specified password to load an encrypted document.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(const System::String &password)
```


| Parameter | Type | Description |
| --- | --- | --- |
| password | const System::String\& | The password to open an encrypted document. Can be null or empty string. |

## Examples



Shows how to encrypt an Html document, and then open it using a password. 
```cpp
// Create and sign an encrypted HTML document from an encrypted .docx.
SharedPtr<CertificateHolder> certificateHolder = CertificateHolder::Create(MyDir + u"morzal.pfx", u"aw");

auto signOptions = MakeObject<SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

String inputFileName = MyDir + u"Encrypted.docx";
String outputFileName = ArtifactsDir + u"HtmlLoadOptions.EncryptedHtml.html";
DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// To load and read this document, we will need to pass its decryption
// password using a HtmlLoadOptions object.
auto loadOptions = MakeObject<HtmlLoadOptions>(u"docPassword");

ASSERT_EQ(signOptions->get_DecryptionPassword(), loadOptions->get_Password());

auto doc = MakeObject<Document>(outputFileName, loadOptions);

ASSERT_EQ(u"Test encrypted document.", doc->GetText().Trim());
```

## See Also

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
