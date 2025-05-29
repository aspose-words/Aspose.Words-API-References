---
title: PersonCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words para .NET
description: Limpie su PersonCollection sin esfuerzo con nuestro método Clear, eliminando al instante todos los elementos para empezar de cero. ¡Simplifique la gestión de sus datos hoy mismo!
type: docs
weight: 50
url: /es/net/aspose.words.bibliography/personcollection/clear/
---
## PersonCollection.Clear method

Elimina todos los elementos de la colección.

```csharp
public void Clear()
```

## Ejemplos

Muestra cómo trabajar con la colección de personas.

```csharp
//Crea una nueva colección de personas.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
//Añadir nueva persona a la colección.
persons.Add(person);
Assert.AreEqual(1, persons.Count);
//Eliminar la persona de la colección si existe.
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

//Crea una colección de personas con dos personas.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
//Eliminar persona de la colección por el índice.
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
//Eliminar todas las personas de la colección.
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### Ver también

* class [PersonCollection](../)
* espacio de nombres [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* asamblea [Aspose.Words](../../../)
