---
title: PersonCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words para .NET
description: Descubra si una PersonCollection incluye a una persona específica con nuestro eficiente método Contiene. ¡Simplifique la gestión de sus datos hoy mismo!
type: docs
weight: 60
url: /es/net/aspose.words.bibliography/personcollection/contains/
---
## PersonCollection.Contains method

Determina si la colección contiene una persona específica.

```csharp
public bool Contains(Person person)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| person | Person | La persona a localizar en la colección. |

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
