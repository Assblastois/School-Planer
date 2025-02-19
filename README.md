# Intorduction / Design philosophy 
This is my School-Planer. It is a fusion between my setup (mainly Dataview, Quickadd and Templater) and the Day Planner plugin. These two parts work side by side, but are strictly separate. The user will link these two parts together! The goal is to not have to create new notes or folder manually. Everythign is done in the background. Just click on the button (done with Note Toolbar)! Handle everything through clean and visually pleasing Dataview tables instead of clicking through folder structures!

![image](https://github.com/user-attachments/assets/64ab0ac8-ca10-4ef9-bf47-9c54cd876637)


## My part
This Vault and Work process relies on the Dataview, Quickadd and Templater plugin. Quickadd and Templater together do the heavy lifting, creating a smooth user experience. Note Toolbar creates the Buttons which activate the macros setting up Notes and Folder structures.

This Vaults structure is intended to be both hierarchical and parallel. 

### Landing Page
On the top you have one note, the Landing page. It displays all the Subjects from either the current semester, or all of them (with the Tabs plugin). (To change the current semester you need to go into the Dataview code block and chose which one you want to display "Semester = x")
I have added the cards CSS from the Minimal Theme, because I like that Dataview look. You can also add an image as the card background, by adding "card-cover" in the Subjects note and adding the image link as the variable:
![image](https://github.com/user-attachments/assets/e8774003-7563-4768-9b3f-3d47682fd66f)

Important, you will also have to add card-cover in the Dataview Query. Having no picture will make the card look a bit ugly though.
![image](https://github.com/user-attachments/assets/02647b23-26a1-4aa6-b4aa-3257c1caf0c9)

### Subject Page:
If you want to create a new Subject you only have to click on the Button on the Landing Page, shown in the image above (Neues Fach). This will prompt you to input the subjects name. After that three folders will be created. [Your Subject], Homework and Knowledge. Due to the macro being complicated and a bit trickey, you will be prompted with two deletion prompts. As soon as you see them, just hit enter, deleting them. I have a 5 second delay built inbetween them popping up, but you need to delete the frist pop-up before the second one. Not managing to to so will result in unspeakable horrors being released. (Deleting the new subject folder and trying again is the easiest way to remedy the situation.)

I use the Folder Notes plugin in this Vault. The Subject has a Folder Note while Homework and Knowledge don't have them; you deleted them when running the New Subject macro. The first thing you should do now is add the semester in the Properties. 
**Important!!** Not doing so, will result in them not being displayed on the Landing Page!! 

The Subject Note is split into three parts: Tests, Homework, Knowledge and completed Homework at the bottom. The Subject Note only serves to display and centralise everything that has to do with that Subject. The real work is done in the Homework and Knowledge notes, which are created by clicking either the Homework (Hausaufgaben) or Knowledge (Wissen) Button.

![image](https://github.com/user-attachments/assets/79cd4de3-8c7b-4b31-9f26-4d15f0a7dc03)


### Homework and Knowledge
This is where the Vault goes form hierarchical to parallel! In both types there will be a backlink to the subject from where they originate. DO NOT DELETE THAT. Otherwise it will not be displayed in the Subject Note's Dataview tables. 

#### Homework
This note is kept fairly simple. The idea is that you put the assignment and your finished work in there. It is up to you how you want to do it. If you want, there is a Handwriting Plugin, which I could not test yet, but which looks very promising. 
You will have to fill out the properties with the due-date (Abgabedatum) and once done the date when you finished (Abschlussdatum), although the later is not necessary. Just something I like to have and see. Once you have finished you also have to tick the checkbox to move it from the open Homework Dataview table to the completed Homework one. 
Lastly, add a task (with "- [ ]" ) and write down what you need to do. This task will be displayed under the To-Do section of the Table.

![image](https://github.com/user-attachments/assets/e7d8e4a9-106e-4a6d-89ab-b3819319b516)


#### Knowledge
This Structure is kept quite simple as well. Put in the name of whatever you are learning or what every knowledge you want to write down. If you like, you can add a small description in the properties (Beschreibung). I have also added a rating system with stars ranging from ⭐ to ⭐⭐⭐⭐⭐. The ranking is displayed on the Subject Note, hopefully motivating you to revisit things you haven't mastered yet! 

It is up to you what and how you want to treat these Knowledge Notes. You can create many small subjects with a high interconnectivity through backlinks, or keep topics broad. 

![image](https://github.com/user-attachments/assets/1cf0c68a-0163-4721-a389-c0a28c298e3a)

## Day Planner
I use the Day Planner to plan my day (haha). I always have it open on the side and when getting an assignment I can directly plan when I will do it. I also have a view of what I'll have to to on a given day. The Daily Notes that are created are all thrown into the Daily Notes Folder. The goal here is that you will not have to navigate to the Daily Notes through the folder or even interact with them, but can access them directly through the Day Planner window. All tasks you have (except for the ones mentioned in the Homework Note) are handled in these Daily Notes.

![image](https://github.com/user-attachments/assets/44fc898b-533b-4fae-98b2-59444adf0e69)
