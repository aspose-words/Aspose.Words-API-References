---
title: 'Aspose::Words::Layout'
second_title: Aspose.Words for C++ API Reference
description: The Aspose.Words.Layout namespace provides classes that allow to access information such as on what page and where on a page particular document elements are positioned, when the document is formatted into pages.
type: docs
weight: 118
url: /cpp/aspose.words.layout/
---

The **Aspose.Words.Layout** namespace provides classes that allow to access information such as on what page and where on a page particular document elements are positioned, when the document is formatted into pages.

## Classes

| Class | Description |
| --- | --- |
| [LayoutCollector](./layoutcollector/) | This class allows to compute page numbers of document nodes. |
| [LayoutEnumerator](./layoutenumerator/) | Enumerates page layout entities of a document. You can use this class to walk over the page layout model. Available properties are type, geometry, text and page index where entity is rendered, as well as overall structure and relationships. Use combination of [GetEntity()](../) and [Current](./layoutenumerator/get_current/) move to the entity which corresponds to a document node. |
| [LayoutOptions](./layoutoptions/) | Holds the options that allow controlling the document layout process. |
| [PageLayoutCallbackArgs](./pagelayoutcallbackargs/) | An argument passed into [Notify()](./ipagelayoutcallback/notify/) |
| [RevisionOptions](./revisionoptions/) | Allows to control how document revisions are handled during layout process. |
## Interfaces

| Interface | Description |
| --- | --- |
| [IPageLayoutCallback](./ipagelayoutcallback/) | Implement this interface if you want to have your own custom method called during build and rendering of page layout model. |
## Enums

| Enum | Description |
| --- | --- |
| [CommentDisplayMode](./commentdisplaymode/) | Specifies the rendering mode for document comments. |
| [ContinuousSectionRestart](./continuoussectionrestart/) | Represents different behaviors when computing page numbers in a continuous section that restarts page numbering. |
| [LayoutEntityType](./layoutentitytype/) | Types of the layout entities. |
| [PageLayoutEvent](./pagelayoutevent/) | A code of event raised during page layout model build and rendering. Page layout model is built in two steps. First, "conversion step", this is when page layout pulls document content and creates object graph. Second, "reflow step", this is when structures are split, merged and arranged into pages. Depending of the operation which triggered build, page layout model may or may not be further rendered into fixed page format. For example, computing number of pages in the document or updating fields does not require rendering, whereas export to Pdf does. |
| [RevisionColor](./revisioncolor/) | Allows to specify color of document revisions. |
| [RevisionTextEffect](./revisiontexteffect/) | Allows to specify decoration effect for revisions of document text. |
| [ShowInBalloons](./showinballoons/) | Specifies which revisions are rendered in balloons. |
