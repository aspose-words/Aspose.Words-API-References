---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs classe"
linktitle: "ImageFieldMergingArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs classe. Fournit des données pour l'événement ImageFieldMerging(). Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class


Fournit des données pour l'événement [ImageFieldMerging()](../ifieldmergingcallback/imagefieldmerging/). Pour en savoir plus, consultez l'article de documentation [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class ImageFieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Renvoie l'objet [Document](../fieldmergingargsbase/get_document/) pour lequel la fusion de courrier est effectuée. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Obtient le nom du champ de fusion tel qu’il est spécifié dans le document. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Obtient l'objet qui représente le champ de fusion actuel. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Obtient le nom du champ de fusion dans la source de données. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Obtient la valeur du champ à partir de la source de données. |
| [get_Image](./get_image/)() const | Spécifie l'image que le moteur de publipostage doit insérer dans le document. |
| [get_ImageFileName](./get_imagefilename/)() const | Définit le nom de fichier de l'image que le moteur de publipostage doit insérer dans le document. |
| [get_ImageHeight](./get_imageheight/)() const | Spécifie la hauteur de l'image à insérer dans le document. |
| [get_ImageStream](./get_imagestream/)() const | Spécifie le flux que le moteur de publipostage doit lire pour obtenir une image. |
| [get_ImageWidth](./get_imagewidth/)() const | Spécifie la largeur de l'image à insérer dans le document. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Obtient l'index basé sur zéro de l'enregistrement qui est fusionné. |
| [get_Shape](./get_shape/)() const | Spécifie la forme que le moteur de publipostage doit insérer dans le document. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Obtient le nom de la table de données pour l'opération de fusion actuelle ou une chaîne vide si le nom n'est pas disponible. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Définit la valeur du champ à partir de la source de données. |
| [set_Image](./set_image/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Spécifie l'image que le moteur de publipostage doit insérer dans le document. |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Définit le nom de fichier de l'image que le moteur de publipostage doit insérer dans le document. |
| [set_ImageHeight](./set_imageheight/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Définisseur pour [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageHeight](./get_imageheight/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Spécifie le flux que le moteur de publipostage doit lire pour obtenir une image. |
| [set_ImageStream](./set_imagestream/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [set_ImageWidth](./set_imagewidth/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Définisseur pour [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth](./get_imagewidth/). |
| [set_Shape](./set_shape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Définisseur pour [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape](./get_shape/). |
| static [Type](./type/)() |  |
## Remarques


Cet événement se produit pendant le publipostage lorsqu'un champ de publipostage d'image est rencontré dans le document. Vous pouvez répondre à cet événement en renvoyant un nom de fichier, un flux ou un objet **Image** au moteur de publipostage afin qu'il soit inséré dans le document.

Trois propriétés sont disponibles [ImageFileName](./get_imagefilename/), [ImageStream](./get_imagestream/) et [Image](./get_image/) pour spécifier d'où l'image doit être prise. Définissez uniquement l'une de ces propriétés.

Pour insérer un champ de publipostage d'image dans un document Word, choisissez la commande Insérer/Champ, puis sélectionnez Champ de fusion et saisissez Image:MyFieldName.

## Voir aussi

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
