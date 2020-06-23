# Creating A Code Snippet

## Text Example

````
We will need to create a small script that allows us to _insert purpose of script_.

Create a new `Script` by selecting `Main Menu -> Assets -> Create -> C# Script` in the Unity software and name it `<script name>`.

Copy and paste the below code into the newly created `<script name>` script:

```
<insert code in codeblock markdown>
```

_insert overview description of script functionality_.

> _insert optional note explaining any specific details of the script functionality_.

Add the `<script name>` script to the `<gameobject>` GameObject.
````

---

> Markdown output example

We will need to create a small script that allows us to _insert purpose of script_.

Create a new `Script` by selecting `Main Menu -> Assets -> Create -> C# Script` in the Unity software and name it `<script name>`.

Copy and paste the below code into the newly created `<script name>` script:

```
<insert code in codeblock markdown>
```

_insert overview description of script functionality_.

> _insert optional note explaining any specific details of the script functionality_.

Add the `<script name>` script to the `<gameobject>` GameObject.

## Final Output

````
### Step X

We will need to create a small script that allows us to change the position of our `Sphere` GameObject to test our newly created `1D Axis Action`.

Create a new `Script` by selecting `Main Menu -> Assets -> Create -> C# Script` in the Unity software and name it `PositionUpdater`.

Copy and paste the below code into the newly created `PositionUpdater` script:

```
using UnityEngine;

public class PositionUpdater : MonoBehaviour
{
    public void SetHorizontalPosition(float newPosition)
    {
        transform.position = Vector3.right * newPosition;
    }
}
```

This simple script has a single method called `SetHorizontalPosition` which will take a `float` value that sets the position of the `Transform` that the script component is on in relation to the left/right axis of the GameObject.

> The `Vector3.right * newPosition` calculation is basically creating a new Vector3 position value based on the world right direction multiplied by the new position value provided. So if `newPosition` was `0` then `Vector3.right` which is a literal of `(0, 0, 1)` would be `(0, 0, 1) * 0 = (0, 0, 0)` and this would set the GameObject position to a world space of `(0, 0, 0)`. If we passed in a newPosition of `1` then the GameObject position will be calculated as `(0, 0, 1)`.

Add the `PositionUpdater` script to the `Sphere` GameObject.
````

---

> Markdown output

### Step X

We will need to create a small script that allows us to change the position of our `Sphere` GameObject to test our newly created `1D Axis Action`.

Create a new `Script` by selecting `Main Menu -> Assets -> Create -> C# Script` in the Unity software and name it `PositionUpdater`.

Copy and paste the below code into the newly created `PositionUpdater` script:

```
using UnityEngine;

public class PositionUpdater : MonoBehaviour
{
    public void SetHorizontalPosition(float newPosition)
    {
        transform.position = Vector3.right * newPosition;
    }
}
```

This simple script has a single method called `SetHorizontalPosition` which will take a `float` value that sets the position of the `Transform` that the script component is on in relation to the left/right axis of the GameObject.

> The `Vector3.right * newPosition` calculation is basically creating a new Vector3 position value based on the world right direction multiplied by the new position value provided. So if `newPosition` was `0` then `Vector3.right` which is a literal of `(0, 0, 1)` would be `(0, 0, 1) * 0 = (0, 0, 0)` and this would set the GameObject position to a world space of `(0, 0, 0)`. If we passed in a newPosition of `1` then the GameObject position will be calculated as `(0, 0, 1)`.

Add the `PositionUpdater` script to the `Sphere` GameObject.