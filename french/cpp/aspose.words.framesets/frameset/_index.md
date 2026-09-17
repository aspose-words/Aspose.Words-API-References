---
title: "Aspose::Words::Framesets::Frameset class"
linktitle: "Frameset"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Framesets::Frameset class. Représente une page de cadres ou un seul cadre sur une page de cadres. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.framesets/frameset/
---
## Frameset class


Représente une page de cadres ou un seul cadre sur une page de cadres. Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Frameset : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Frameset](./frameset/)() |  |
| [get_ChildFramesets](./get_childframesets/)() const | Obtient la collection des cadres enfants et des pages de cadres. |
| [get_FrameDefaultUrl](./get_framedefaulturl/)() | Obtient ou définit l'URL de la page Web ou le nom de fichier du document à afficher dans ce cadre. |
| [get_IsFrameLinkToFile](./get_isframelinktofile/)() | Obtient ou définit une valeur indiquant si la page Web ou le nom de fichier du document spécifié dans la propriété [FrameDefaultUrl](./get_framedefaulturl/) est une ressource externe à laquelle le cadre est lié. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FrameDefaultUrl](./set_framedefaulturl/)(const System::String\&) | Définisseur pour [Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl](./get_framedefaulturl/). |
| [set_IsFrameLinkToFile](./set_isframelinktofile/)(bool) | Définisseur pour [Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile](./get_isframelinktofile/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment accéder aux cadres sur la page.
```cpp
// Le document contient plusieurs cadres avec des liens vers d'autres documents.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Frameset.docx");

ASSERT_EQ(3, doc->get_Frameset()->get_ChildFramesets()->get_Count());
// Nous pouvons vérifier l'URL par défaut (une URL de page Web ou un document local) ou si le cadre est une ressource externe.
ASSERT_EQ(u"https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_FrameDefaultUrl());
ASSERT_TRUE(doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_IsFrameLinkToFile());

ASSERT_EQ(u"Document.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_FrameDefaultUrl());
ASSERT_FALSE(doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_IsFrameLinkToFile());

// Modifiez les propriétés d'un de nos cadres.
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_FrameDefaultUrl(u"https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_IsFrameLinkToFile(false);
```

## Voir aussi

* Namespace [Aspose::Words::Framesets](../)
* Library [Aspose.Words for C++](../../)
