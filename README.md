# Redirecting-the-scene

## Aim:
 To Redirect the scene in the unity engine.
## Algorithm:
### Step 1 :
To open the unity engine.
### step 2:
Create a new plane and create a cube and give color for the cube.
### Step 3:
Next create sphere in the orgin and change the z-axis and Give the color for the sphere.
### Step 4:
Create a tag for the Sphere and Make the sphere and cube as a Rigidbodies and Make the sphere use Gravity
## Step 5:
Create the C# script file in the Assets and write the Coding for the Redirecting to the page2 after hit the sphere to cube.
### Step 6:
Next Create a another new scene named as page2.
### Step 7:
In File->Build settings and drop the both first scene and page2 scene in the Scenes in build setting.
### Step 8:
Click the Build and run button in the Build settings and run the scene.
### Step 9:
The Sphere after touching the cube it will disappeared and Press the key [R] the redircting to the new scene that is page2.
## Program:
~~~
using System.Collections;
using System.Collections.Generic;
using UnityEngine.SceneManagement;
using UnityEngine;

public class CubeProg : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("level2");
        }
    }
    public void OnMouseDown()
    {
        Destroy(gameObject);
    }
    private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "cube")
        {
            Destroy(collision.gameObject);
            WinText.SetActive(true);
        }
    }
}
~~~
## Output:
## Scene 1:
![e1](https://github.com/21005984/Redirecting-the-scene/assets/94748389/6bb8e45c-69f3-440e-8e39-7d515bda6119)

## After the bal hits the cube
![e2](https://github.com/21005984/Redirecting-the-scene/assets/94748389/efebc4ad-f92d-49ea-8fe6-d7fa5068fd3d)

## Redirected to scene 2:
![e3](https://github.com/21005984/Redirecting-the-scene/assets/94748389/7885a297-e22b-465f-b2c8-ea59e12c2f90)

## Result:
The above C# coding is successfully redirecting the scene in the unity engine.
