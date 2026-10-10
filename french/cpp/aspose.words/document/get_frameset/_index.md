---
title: "Aspose::Words::Document::get_Frameset méthode"
linktitle: "get_Frameset"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_Frameset méthode. Retourne une instance Frameset si ce document représente une page à cadres en C++."
type: docs
weight: 27000
url: /fr/cpp/aspose.words/document/get_frameset/
---
## Document::get_Frameset method


Retourne une instance [Frameset](./) si ce document représente une page à cadres.

```cpp
System::SharedPtr<Aspose::Words::Framesets::Frameset> Aspose::Words::Document::get_Frameset() const
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

* Class [Frameset](../../../aspose.words.framesets/frameset/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
