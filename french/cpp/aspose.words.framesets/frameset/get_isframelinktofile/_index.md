---
title: "Méthode get_IsFrameLinkToFile de Aspose::Words::Framesets::Frameset"
linktitle: "get_IsFrameLinkToFile"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode get_IsFrameLinkToFile de Aspose::Words::Framesets::Frameset. Obtient ou définit une valeur indiquant si la page Web ou le nom du fichier de document spécifié dans la propriété FrameDefaultUrl est une ressource externe à laquelle le cadre est lié en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.framesets/frameset/get_isframelinktofile/
---
## Frameset::get_IsFrameLinkToFile method


Obtient ou définit une valeur indiquant si la page Web ou le nom du fichier de document spécifié dans la propriété [FrameDefaultUrl](../get_framedefaulturl/) est une ressource externe à laquelle le cadre est lié.

```cpp
bool Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile()
```


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

* Class [Frameset](../)
* Namespace [Aspose::Words::Framesets](../../)
* Library [Aspose.Words for C++](../../../)
