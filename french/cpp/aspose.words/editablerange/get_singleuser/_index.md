---
title: "Méthode Aspose::Words::EditableRange::get_SingleUser"
linktitle: "get_SingleUser"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::EditableRange::get_SingleUser. Retourne ou définit l'utilisateur unique pour la plage modifiable en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/editablerange/get_singleuser/
---
## EditableRange::get_SingleUser method


Renvoie ou définit l'utilisateur unique pour la plage éditable.

```cpp
System::String Aspose::Words::EditableRange::get_SingleUser()
```

## Remarques


Cet éditeur peut être stocké sous l'une des formes suivantes :

DOMAIN\\Username - pour les utilisateurs dont l'accès doit être authentifié à l'aide des informations d'identification du domaine de l'utilisateur actuel.

user@domain.com - pour les utilisateurs dont l'accès doit être authentifié à l'aide de l'adresse e-mail de l'utilisateur comme informations d'identification.

user - pour les utilisateurs dont l'accès doit être authentifié à l'aide des informations d'identification de la machine de l'utilisateur actuel.

L'utilisateur unique et le groupe d'éditeurs ne peuvent pas être définis simultanément pour la plage modifiable spécifique ; si l'un est défini, l'autre sera effacé.
## Voir aussi

* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
