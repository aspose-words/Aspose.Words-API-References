---
title: PersonCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words para .NET
description: Añade fácilmente una persona a tu colección con el método PersonCollection Add. ¡Optimiza la gestión de datos y mejora la eficiencia de tu proyecto!
type: docs
weight: 40
url: /es/net/aspose.words.bibliography/personcollection/add/
---
## PersonCollection.Add method

Agrega un[`Person`](../../person/) a la colección.

```csharp
public void Add(Person person)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| person | Person | La persona que se agregará a la colección. |

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

* class [Person](../../person/)
* class [PersonCollection](../)
* espacio de nombres [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* asamblea [Aspose.Words](../../../)
