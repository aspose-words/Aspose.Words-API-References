---
title: "Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf Methode"
linktitle: "get_SaveImagesAsWmf"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf Methode. Wenn true werden alle Bilder als WMF in C++ gespeichert."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/rtfsaveoptions/get_saveimagesaswmf/
---
## RtfSaveOptions::get_SaveImagesAsWmf method


Wenn **true**, werden alle Bilder als WMF gespeichert.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf() const
```


## Beispiele



Zeigt, wie man alle Bilder in einem Dokument in das Windows Metafile-Format konvertiert, während wir das Dokument als RTF speichern.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jpeg image:");
System::SharedPtr<Aspose::Words::Drawing::Shape> imageShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imageShape->get_ImageData()->get_ImageType());

builder->InsertParagraph();
builder->Writeln(u"Png image:");
imageShape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, imageShape->get_ImageData()->get_ImageType());

// Erstellen Sie ein \"RtfSaveOptions\"‑Objekt, das an die \"Save\"‑Methode des Dokuments übergeben wird, um zu ändern, wie wir es als RTF speichern.
auto rtfSaveOptions = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

// Setzen Sie die Eigenschaft "SaveImagesAsWmf" auf "true", um alle Bilder im Dokument beim Speichern als RTF in WMF zu konvertieren.
// Damit wird Lesern wie WordPad geholfen, unser Dokument zu lesen.
// Setzen Sie die Eigenschaft "SaveImagesAsWmf" auf "false", um das Originalformat aller Bilder im Dokument beizubehalten
// wenn wir es als RTF speichern. Dies bewahrt die Bildqualität, jedoch zulasten der Kompatibilität mit älteren RTF-Lesern.
rtfSaveOptions->set_SaveImagesAsWmf(saveImagesAsWmf);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"RtfSaveOptions.SaveImagesAsWmf.rtf");

System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

if (saveImagesAsWmf)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Wmf, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0)))->get_ImageData()->get_ImageType());
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Wmf, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0)))->get_ImageData()->get_ImageType());
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1)))->get_ImageData()->get_ImageType());
}
```

## Siehe auch

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
