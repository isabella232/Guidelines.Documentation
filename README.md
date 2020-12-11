# Documentation Guidelines

> A collection of guides and examples of how to structure documentation

## Introduction

This is a guide to show how to structure the documentation and a collection of reusable patterns of how to describe certain actions carried out in documentation. It also provides useful descriptions of how to create the relevant graphics for the guides as well.

## Generic Structure

### Overview

The overview outlines the basic parameters of the guide, such as the level of who the guide is aimed at, the amount of time to read through the guide and any other relevant information.

For a Unity project, the overview should be a bullet point list formatted as a note describing the relevant data.

**Example**

```
> * Level: Beginner
>
> * Reading Time: 2 minutes
>
> * Checked with: Unity 2018.3.14f1
```

The markdown will be rendered like so:

> * Level: Beginner
>
> * Reading Time: 2 minutes
>
> * Checked with: Unity 2018.3.14f1

### Introduction

The introduction should give a brief explanation of what the guide is teaching and the outcomes to expect. It should also cover any potential variations of different prefabs that can be swapped out in the guide.

### Prerequisites

The prerequisites describe any prior setup required before the guide can be followed, such examples are another guide has been followed and the project that you're working on has been set up. The prerequisites are a bullet point list, with any links in the text to be outlined at the bottom of the markdown file.

**Example**

```
* [Add the Tilia.Interactions.Interactables.Unity -> Interactions.Interactor] prefab to the scene Hierarchy.
* [Install the Tilia.Interactions.Interactables.Unity] package dependency in to your [Unity] project.
```

The markdown will be rendered like so:

* [Add the Tilia.Interactions.Interactables.Unity -> Interactions.Interactor] prefab to the scene Hierarchy.
* [Install the Tilia.Interactions.Interactables.Unity] package dependency in to your [Unity] project.

The links in the bullet points need adding to the bottom of the markdown file.

```
[Add the Tilia.Interactions.Interactor.Unity -> Interactions.Interactor]: https://github.com/ExtendRealityLtd/Tilia.Interactions.Interactables.Unity/tree/master/Documentation/HowToGuides/AddingAnInteractor
[Install the Tilia.Interactions.Interactables.Unity]: ../Installation/README.md
```

[Add the Tilia.Interactions.Interactor.Unity -> Interactions.Interactor]: https://github.com/ExtendRealityLtd/Tilia.Interactions.Interactables.Unity/tree/master/Documentation/HowToGuides/AddingAnInteractor
[Install the Tilia.Interactions.Interactables.Unity]: ../Installation/README.md

### The Guide

All guides are split into multiple steps that come under the **Let's Start** header and then each step is a sub header. Any images required are linked inline, but any page hyperlinks should have their links placed at the bottom of the markdown file.

The final step of _The Guide_ should be the `### Done` section, which outlines the results and any conclusions that the guide.

```
## Let's Start

### Step 1

The guide text goes here.

![Image Description Should Describe What Is Going On](assets/images/ImageDescriptionShouldDescribeWhatIsGoingOn.png)

### Step 2

The guide text goes here.

![Image Description Should Describe What Is Going On](assets/images/ImageDescriptionShouldDescribeWhatIsGoingOn.png)

### Done

The guide text goes here.

![Image Description Should Describe What Is Going On](assets/images/ImageDescriptionShouldDescribeWhatIsGoingOn.png)
```

#### Images

Images should clearly show the step in a simple graphical way and should be in `PNG8` image format.

The filename of the image should describe what is going on in the image so that screen readers can convey the message of the image to those who are visually impaired. The filename should be in PascalCase (the first letter of each word should be uppercase) and there should be no spaces between each word.

The link description for the image should be identical to the filename except it **should** have spaces between the words in the name.

#### Common Guide Actions

Most guides have the same actions in principle just with the specifics changed slightly. The wording of these steps should be formalized so the guides are consistent and easier to read.

1. [Adding A Package To A Scene](Documentation/CommonGuideActions/AddingAPackageToAScene/README.md)
2. [Adding A Component To A GameObject](Documentation/CommonGuideActions/AddingAComponentToAGameObject/README.md)
3. [Creating A Unity Primitive](Documentation/CommonGuideActions/CreatingAUnityPrimitive/README.md)
4. [Creating A Code Snippet](Documentation/CommonGuideActions/CreatingACodeSnippet/README.md)
5. [Dragging A GameObject To A Component Property](Documentation/CommonGuideActions/DraggingAGameObjectToAComponentProperty/README.md)
6. [Updating A Component Property Value](Documentation/CommonGuideActions/UpdatingAComponentPropertyValue/README.md)
7. [Updating A Component List Property](Documentation/CommonGuideActions/UpdatingAComponentListProperty/README.md)
8. [Adding A Unity Event Listener](Documentation/CommonGuideActions/AddingAUnityEventListener/README.md)
9. [Updating A Unity Event Listener](Documentation/CommonGuideActions/UpdatingAUnityEventListener/README.md)
10. [Resetting Component Property Back To None](Documentation/CommonGuideActions/ResettingComponentPropertyBackToNone/README.md)
11. [Showing The Scene](Documentation/CommonGuideActions/ShowingTheScene/README.md)

### Common Patterns

* Arrows in screenshots should only be used to convey motion e.g. dragging and dropping.
* Pink outline boxes should be used to highlight an area that is a property that can be changed or a button that can be clicked.
* GameObject paths should always be the complete hierarchy path e.g. `TopLevelObject -> ChildObject -> ActualObject`.

### Common Word Styling

* Unity should always start with an uppercase `U` and the first occurrence of the word should be linked to the [Unity](https://unity.com/) website.
* GameObject should always be uppercase `G` and uppercase `O` and not highlighted in a code block.
* Any Unity window/tab label should start with an uppercase letter:
  * `Project` - Unity Project window.
  * `Hierarchy` - Unity Hierarchy window, Unity scene Hierarchy, from the Unity Hierarchy, etc.
  * When the word hierarchy is used and not referring to the Unity Hierarchy window, it should be lowercase `h` unless at the start of a sentence then should be a capitalized `H`.
* When a function of Unity is referred to, always refer to it as the Unity software
  * Correct: `do functionX in the Unity software.`
  * Incorrect: `do functionX in Unity.`
* Field values are always referred to as property and in lowercase.
* Components are referred to as component and in lowercase.