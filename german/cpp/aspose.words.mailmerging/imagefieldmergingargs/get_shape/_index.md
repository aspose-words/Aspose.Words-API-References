---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape Methode"
linktitle: "get_Shape"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape Methode. Gibt die Form an, die die Seriendruck‑Engine in das Dokument in C++ einfügen muss."
type: docs
weight: 7000
url: /de/cpp/aspose.words.mailmerging/imagefieldmergingargs/get_shape/
---
## ImageFieldMergingArgs::get_Shape method


Gibt die Form an, die die Seriendruck-Engine in das Dokument einfügen muss.

```cpp
const System::SharedPtr<Aspose::Words::Drawing::Shape> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape() const
```

## Hinweise


Wenn diese Eigenschaft angegeben ist, ignoriert die Seriendruck‑Engine alle anderen Eigenschaften wie [ImageFileName](../get_imagefilename/) oder [ImageStream](../get_imagestream/) und fügt einfach die Form in das Dokument ein.

Verwenden Sie diese Eigenschaft, um den Vorgang des Zusammenführens eines Bild‑Seriendruckfeldes vollständig zu steuern. Zum Beispiel können Sie [WrapType](../../../aspose.words.drawing/shapebase/get_wraptype/) oder jede andere Formeigenschaft angeben, um den resultierenden Knoten fein abzustimmen. Bitte beachten Sie jedoch, dass Sie für die Bereitstellung des Inhalts der Form verantwortlich sind.
## Siehe auch

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
