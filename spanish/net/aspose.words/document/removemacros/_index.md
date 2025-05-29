---
title: Document.RemoveMacros
linktitle: RemoveMacros
articleTitle: RemoveMacros
second_title: Aspose.Words para .NET
description: Elimine sin esfuerzo todas las macros, barras de herramientas y configuraciones de comandos personalizados de su proyecto VBA con el método Document RemoveMacros para obtener un documento más limpio.
type: docs
weight: 720
url: /es/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Elimina todas las macros (del proyecto VBA), así como las barras de herramientas y las personalizaciones de comandos del documento.

```csharp
public void RemoveMacros()
```

## Observaciones

Al eliminar todas las macros de un documento, puede asegurarse de que el documento no contenga virus de macro.

## Ejemplos

Muestra cómo eliminar todas las macros de un documento.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

//Elimine el proyecto VBA del documento, junto con todas sus macros.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
