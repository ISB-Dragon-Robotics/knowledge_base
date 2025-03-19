---
description: >-
  Information by George Xu (ISB) and Jun Lee (VEXU Team ILLINI), reformatted by
  Samuel Yao (ISB) and George Xu (ISB)
---

# Fusion 360 for V5RC Intro

## Fusion360 Installation Guide

Fusion 360 is typically very expensive. However, students may acquire Education Edition without any cost. If you do not have an Autodesk account, you will need to do so before beginning this process. When you do so, you must use the name that will be shown on your school report card

Once you have logged in, head to the education section [here](https://www.autodesk.com/education/edu-software/overview), where you should click "select" under the section "Fusion", as seen below.

<figure><img src="../../.gitbook/assets/Screen Shot 2025-01-15 at 16.14.46.png" alt=""><figcaption><p>Click on the circled button</p></figcaption></figure>

Next, click the "Access Products" button shown:

<figure><img src="../../.gitbook/assets/Screen Shot 2025-01-15 at 16.16.35.png" alt=""><figcaption><p>Click on the button</p></figcaption></figure>

You will now be shown a variety of options. For now, select only the base "Fusion" option. Your account should have the text "Access" instead of "Download" if you have not acquired Fusion yet. I will provide&#x20;

<figure><img src="../../.gitbook/assets/Screen Shot 2025-01-15 at 16.18.38.png" alt=""><figcaption><p>Click on the button</p></figcaption></figure>

Please follow their instruction and provide a piece of evidence for your student status. You should recieve a student license in 1-2 days

## Computer Recommendations

&#x20;It is important to have a good CPU. A mistake made by many beginners is to invest in a powerful GPU. Fusion will not use the GPU unless you are using their raytracing rendering feature, which is useless during design. The most important spec for Fusion is the single-thread performance. The application is not optimized to take advantage of core count. Having at least 16GB, preferably 32GB, of RAM is needed for large VEX models. Make sure your internet is also very good as Fusion relies heavily on online tools and saves to store your designs.

## Fusion Best Practices

In Fusion, it is best to reduce the amount of actual decisions. If an item must be deleted, go back to the "Fusion timeline" at the bottom of the screen and undo the addition instead of deleting the item at the end of the timeline. This reduces the load time as fusion evaluates each step by recalculating all of your past edits.

You should also try to group items into either components or into their own individual file. For example, a specific combination of wheels and gears that is used repeatedly may be converted into an individual CAD file to make it easier to retrieve. The base as a whole may be grouped into a single component to help visualization: By hiding the entire base component, it is easier and faster to edit the parts above the base.

Only one person can work on each file at a time. If multiple people modify a file at the same time, some changes will not be saved. Make sure to save your work before closing Fusion as autosave is not a available function. Talk to your teammates if multiple people are working on the same project. Under document settings, you can change active units. **Always use inches in vex.**

## Setting up Fusion 360

&#x20;![](<../../.gitbook/assets/Screen Shot 2025-03-19 at 13.09.58.png>)

When setting up a project, you may find a list on the sidebar, shown above. You can click "New Project", which we have done to create the "ISB CAD" project.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeWUX36EwRiGXN1XMkgowMUR98Gq_oILhCv0RCAv4isjLHObREgyOaV45U2EpIAjF9z9bXOiSSZjstAC7KLSdIPtOME5EnluenfagbIaG-iWhfcHp5jdaroorJeBEGssryN1C3uig?key=YgGEmF37zgO5qhrHs4oU9jHT)

As seen above, it is possible to create folders inside the project, making it easier to find certain parts.

It is very important to remember that only one person can work on each file at a time. If multiple people modify a file at the same time, some changes will not be saved. Make sure to save your work before closing Fusion. Talk to your teammates if multiple people are working on the same project.&#x20;

One method to reduce errors is to copy a file and make adjustments there. Make sure to update the primary robot and delete the temporary file when you are done, preventing your fusion file from becoming overly messy after a few rounds of duplication.&#x20;

## General Fusion Info

Under document settings, you can change active units. Always use inches in vex.&#x20;

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdmZ3A7GnEYSbvZ1BruHXUYOqMZkoxBn22h0i-0oqLxZ1_fWWX5tTln5qZu2BmmnrVTPNXQS1KhIgEkGwOHRKOKrohyfC9c_lLxEbZBQuKjjOm6MWzUBvq3DSgWwu_iJhXdmZw9Cg?key=YgGEmF37zgO5qhrHs4oU9jHT)

Head to the bottom corner. You can change your visual style based on personal preference.&#x20;

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXckyIBDMCe8knT6WcH4m3f_YvIAHa96NKtFw2p9-6nWerPT0uze8gwgHcmlLU6MS9dOEl_QZLkl6WezQW1PlXpXH1Svk56maPVhAghH_OflIczcHVu_onXxciMjPL3YzhNvqKJWLA?key=YgGEmF37zgO5qhrHs4oU9jHT)

You can drag this cube (top right) to rotate the working environment.&#x20;

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdRBNNi_tf7Zi2tvaquKZm6L_zc-vnYHpqzErTfRI6J_tI50RpdkoEv2CsbtjecY2clvnXwaEGcXMNS4R-RbiUDJRnI_NYR3Y6WdOTU3XF18BfbZ0aKzUCm_SeuSQ_qv5x_23cXzQ?key=YgGEmF37zgO5qhrHs4oU9jHT)

Click on the triangle next to the cube and click Orthographic.&#x20;

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdC85SsC6fo3U9wEZS_WGwNM8DrjlWoC1RtDNp2gTyiNKmdTCuAZlfwLqp0jWMJmgAAZWp11k6HuDARqw6N8Qc_wn4xBs70TOs-KoAB2s25zM9327rs-aFFKryFdKoSjmkiEOt46w?key=YgGEmF37zgO5qhrHs4oU9jHT)

Orthographic doesn’t account for where the part is. Everything is scaled to have the same unit length on your screen. Perspective accounts for distance and shows a more realistic model. If orthographic makes you dizzy, change to perspective.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcRX3JrZ1LeS6xgn_5t7GuTFqS1egs7ML9y4B1uiYeECsnUWP3xNEkUPIMuokMENJ66Pmnvw7DRdH0XgHdCI6zWo3c55wVcUkIBDrxcI-uzlqO0sLNU6FbhJYPJw4mdiDK7Qse-Kw?key=YgGEmF37zgO5qhrHs4oU9jHT)\
\
Using inspect, you can select two planes or points and measure the length between them.&#x20;

Using Interference, you can select parts and check if they have any interference.&#x20;

Using Section Analysis, you can pick and plane and see a x-ray-like view of your design.

## How to VEX CAD

In this section, I’ll be going over how to assemble VEX parts. First, please follow [this video guide](https://www.youtube.com/watch?v=DhSNF_7SHcA&) to install the VEX Fusion Library. It is best to put this into a specific folder to make it easier to navigate and harder to accidentally edit a part.

1. First make a new design (command+N) and save in your team folder (command+S). Name the design “Chassis yourname” and put the location as “ISB CAD> yourteam”
2. Click the following folders to navigate all the 2-wide C channels. ISB CAD -> VEX parts -> Structure -> Aluminum -> 2x C-Channel
3. Hover over 20-2x C-Chan and right-click.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXexKuZubgAhCEjuteNfGDrbru5iRdaV7ubyMYFsR6AmzOcaYptKTeZE8irnVIjYMyzABZ4a0IX7ejojWKd3v0oEhZCqY8ClBK367mtf3TLJFiUosLrgXek3D8Mbc98J1aFooucS?key=YgGEmF37zgO5qhrHs4oU9jHT)

If you want to use parts from the vex library, you need to click “Insert into Current Design” or drag the part into the specific design you are working on. This library is a bunch of pre-made parts and brings your needed parts to your folder. So in reality, everyone is sharing the same part. PLEASE DO NOT MAKE ANY CHANGES UNDER VEX PARTS.

4. Rotate the C channel so that it faces you and click OK.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcJZTH4IiugmkjrRgcvHV8gSRA8R4nqp73uUogYWlD7Mup7HSAXk4d_xNvqic7FjpbMrmWHYmv7ax-b50qd4BeHFl4udeCE4yShDXqh0AjGtefzx8mzTVCzMazBMWUFAW5oYCVx?key=YgGEmF37zgO5qhrHs4oU9jHT)

5. Repeat the same step and find&#x20;

VEX parts > Hardware > Screws > 8-32 > Steel > 0.5 Star Screw. Add the part into the design again

Click and drag the upward facing arrow. This will move the part upwards. Alternatively, click on the flat rectangles to drag it along a plane.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcHtMeQbRY1o1veGhsXEX3VgrVYIpcSJ3hZqkbkX6-OMQZVbjnIJVedmDrESQB_b-8HPb3fmv5tfKOauMZIIyrnHWbynHhlrcM9su7f7kwQjGPXw2lnw3r8pSdmJGZTXVbppRsuIw?key=YgGEmF37zgO5qhrHs4oU9jHT)

Click OK one the part is fully visible.

6. Under the ASSEMBLE tab, click “Joint", which is the blue highlighted option below.

<div align="left"><figure><img src="../../.gitbook/assets/Screen Shot 2025-03-19 at 13.24.34.png" alt=""><figcaption></figcaption></figure></div>

7. The align feature selects two points, From and To, and puts them together.&#x20;

First hover over the plane where your desired point is. In this case, we want to put a screw on the C-Channel. First picture where the screw contacts the C-Channel.&#x20;

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdz01VAl0xj-ki6aXMAIw7gVuzyVFc7dwL7GCNhkZxdkdYhS8dIuBUcCmVVB1qWu3yVtQzk0uqP59kwhv63Fo9xkF6m68w1dj92ApLYAqMum3aB8JSed4QtzhnDyGpixtMy32fHsA?key=YgGEmF37zgO5qhrHs4oU9jHT)

If you press “Command”, it should show you all the points you can select. In most cases, you can just hover over the point you want to select, and Fusion should have it ready. But sometimes, these points can be missing, overlapping with another part, or hard to locate. Using the Command feature will always show the points on the plate you are hovering over.&#x20;

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfKoj2gXmXOLUja_xPNLdZBLYurlSmcljnyqvd4AScAH8jZQBfsIBZzF5iVV-sYeqtCA1idrbNF7r4vyeIy-58D5VBRN53rjF0HYJTVqIIlfn63JPNJDrKfjstJz7jbCFz1MPeb?key=YgGEmF37zgO5qhrHs4oU9jHT)

Click on the blue cross.&#x20;

8. Click on any of the dots on the c-channel

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdCYC3re5HNjC9zYuqkVefGF2Ew4k0DKRVb3YIIEnDHd8Xsstug6r8JgkhOD0oUoW8DzMW07VtaogVGytcHVgf8HxRV9Yaq9Ono-wOBbOuBkrXfhLvMRilcR539gsGOse-K-l5r_g?key=YgGEmF37zgO5qhrHs4oU9jHT)

If the geometry of the parts is not correct, you can further adjust these using these tools. You can also click on the "X" next to "From" to cancel and reselect your points. Click OK when you are happy. You may also go into the motion tab to select how the joint works. Play around with different joint types to better understand it.

<div align="left"><figure><img src="../../.gitbook/assets/Screen Shot 2025-03-19 at 13.24.15 (1).png" alt="" width="304"><figcaption></figcaption></figure></div>

9. This is what the final version should look like.&#x20;

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfSfCiWNvILe0aowopP1WwsSk4KUY_D0cUomIr0W90-_6i4wFUGVRKMaZ4U1XaBvgyONdEaMG1xVrDwqzvkSsdJE_ZYeNVaD8uCDQUm4fQ-3jOf85yPuu8deEPdyq0DhV7_VN7NaQ?key=YgGEmF37zgO5qhrHs4oU9jHT)

Now try adding a thin nylon but on the other side of the screw. You can insert any parts such as motors, and wheels to build your robot. Click on all the folders under vex cad to be comfortable with where all the parts are.&#x20;

You can now use these techniques to design any VEX robot. It is highly recommended to join the VEX Fusion discord.

