---
title: CustomDocumentProperties.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words pour .NET
description: Créez facilement des propriétés de document personnalisées uniques grâce à la méthode Add. Améliorez vos documents avec des types de données String personnalisés pour des performances optimales.
type: docs
weight: 10
url: /fr/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(*string, string*) {#add_4}

Crée une nouvelle propriété de document personnalisée duString type de données.

```csharp
public DocumentProperty Add(string name, string value)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Le nom de la propriété. |
| value | String | La valeur de la propriété. |

### Return_Value

L'objet de propriété nouvellement créé.

## Exemples

Montre comment travailler avec les propriétés personnalisées d'un document.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Les propriétés de document personnalisées sont des paires clé-valeur que nous pouvons ajouter au document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprimez chaque propriété personnalisée dans le document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Affichez la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" -> "Propriétés avancées" -> "Personnalisé".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Vous trouverez ci-dessous trois manières de supprimer les propriétés personnalisées d'un document.
// 1 - Supprimer par index :
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Supprimer par nom :
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vider toute la collection en une seule fois :
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Voir également

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*string, int*) {#add_2}

Crée une nouvelle propriété de document personnalisée duNumber type de données.

```csharp
public DocumentProperty Add(string name, int value)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Le nom de la propriété. |
| value | Int32 | La valeur de la propriété. |

### Return_Value

L'objet de propriété nouvellement créé.

## Exemples

Montre comment travailler avec les propriétés personnalisées d'un document.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Les propriétés de document personnalisées sont des paires clé-valeur que nous pouvons ajouter au document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprimez chaque propriété personnalisée dans le document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Affichez la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" -> "Propriétés avancées" -> "Personnalisé".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Vous trouverez ci-dessous trois manières de supprimer les propriétés personnalisées d'un document.
// 1 - Supprimer par index :
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Supprimer par nom :
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vider toute la collection en une seule fois :
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Voir également

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*string, DateTime*) {#add_3}

Crée une nouvelle propriété de document personnalisée duDateTime type de données.

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Le nom de la propriété. |
| value | DateTime | La valeur de la propriété. |

### Return_Value

L'objet de propriété nouvellement créé.

## Exemples

Montre comment créer une propriété de document personnalisée contenant une date et une heure.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

Montre comment travailler avec les propriétés personnalisées d'un document.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Les propriétés de document personnalisées sont des paires clé-valeur que nous pouvons ajouter au document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprimez chaque propriété personnalisée dans le document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Affichez la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" -> "Propriétés avancées" -> "Personnalisé".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Vous trouverez ci-dessous trois manières de supprimer les propriétés personnalisées d'un document.
// 1 - Supprimer par index :
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Supprimer par nom :
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vider toute la collection en une seule fois :
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Voir également

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*string, bool*) {#add}

Crée une nouvelle propriété de document personnalisée duBoolean type de données.

```csharp
public DocumentProperty Add(string name, bool value)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Le nom de la propriété. |
| value | Boolean | La valeur de la propriété. |

### Return_Value

L'objet de propriété nouvellement créé.

## Exemples

Montre comment travailler avec les propriétés personnalisées d'un document.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Les propriétés de document personnalisées sont des paires clé-valeur que nous pouvons ajouter au document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprimez chaque propriété personnalisée dans le document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Affichez la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" -> "Propriétés avancées" -> "Personnalisé".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Vous trouverez ci-dessous trois manières de supprimer les propriétés personnalisées d'un document.
// 1 - Supprimer par index :
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Supprimer par nom :
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vider toute la collection en une seule fois :
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Voir également

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*string, double*) {#add_1}

Crée une nouvelle propriété de document personnalisée duDouble type de données.

```csharp
public DocumentProperty Add(string name, double value)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| name | String | Le nom de la propriété. |
| value | Double | La valeur de la propriété. |

### Return_Value

L'objet de propriété nouvellement créé.

## Exemples

Montre comment travailler avec les propriétés personnalisées d'un document.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Les propriétés de document personnalisées sont des paires clé-valeur que nous pouvons ajouter au document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Imprimez chaque propriété personnalisée dans le document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Affichez la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" -> "Propriétés avancées" -> "Personnalisé".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Vous trouverez ci-dessous trois manières de supprimer les propriétés personnalisées d'un document.
// 1 - Supprimer par index :
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Supprimer par nom :
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Vider toute la collection en une seule fois :
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Voir également

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../../aspose.words.properties/)
* Assemblée [Aspose.Words](../../../)
