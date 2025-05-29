---
title: PersonCollection
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: Aspose.Words para .NET
description: Cree y administre una colección dinámica de individuos con la clase PersonCollection. ¡Simplifique la gestión de datos y mejore sus aplicaciones hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words.bibliography/personcollection/personcollection/
---
## PersonCollection() {#constructor}

Inicializar una nueva instancia del[`PersonCollection`](../) clase.

```csharp
public PersonCollection()
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

---

## PersonCollection(*IEnumerable&lt;Person&gt;*) {#constructor_2}

```csharp
public PersonCollection(IEnumerable<Person> persons)
```

### Ver también

* class [Person](../../person/)
* class [PersonCollection](../)
* espacio de nombres [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* asamblea [Aspose.Words](../../../)

---

## PersonCollection(*params Person[]*) {#constructor_1}

Inicializar una nueva instancia del[`PersonCollection`](../) clase.

```csharp
public PersonCollection(params Person[] persons)
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

* class [Person](../../person/)
* class [PersonCollection](../)
* espacio de nombres [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* asamblea [Aspose.Words](../../../)
