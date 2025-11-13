# GAME_PROGRAM-EX--5
# MAKING PLAYER TO COLLECT THE AMMO AND INCREASE THE BULLET SPAWN COUNT.
# NAME : HALIMA HARISHA A 
# REGISTER NO : 212224040094
# AIM :
To implement a gameplay feature where the player collects ammo pickups in the game world. Upon collecting ammo, the player's ammo count increases, enabling more bullet spawns (shots).

# PROCEDURE :
1. Setup Player Character

• Open your PlayerCharacter Blueprint.




• Add a new Integer variable named AmmoCount.





• Set an initial default value (e.g., AmmoCount = 10).





• Ensure you have a shooting mechanism in place that uses AmmoCount to determine if a bullet can be fired.

2. Create Ammo Pickup Blueprint

• Go to the Content Browser → Right-click → Blueprint Class → Select Actor → Name it BP_AmmoPickup.

• Add components:





 ○ Static Mesh: Representing the ammo (e.g., a bullet or crate).




 
 ○ Sphere Collision: To detect overlap with the player.

• In the Event Graph of BP_AmmoPickup:




 ○ Use OnComponentBeginOverlap on the Sphere Collision.




 
 ○ Cast to PlayerCharacter.



 
 ○ Increase the player’s AmmoCount (e.g., AmmoCount += 5).



 
 ○ Optionally, play a pickup sound or effect.




 
 ○ Destroy the ammo pickup actor.

3. Update Shooting Logic (Optional)

• In your player’s shooting logic:




 ○ Before spawning a bullet, check if AmmoCount > 0.



 
 ○ If true:


 
  ▪ Spawn bullet.



  
  ▪ Decrease AmmoCount by 1.

  

4. Place Ammo in the World

• Drag instances of BP_AmmoPickup into your level from the Content Browser.







• Adjust position, mesh, and pickup range as needed.






# OUTPUT :

<img width="1135" height="498" alt="image" src="https://github.com/user-attachments/assets/c770dfef-3fe6-46b5-9cda-7e38e5227aab" />

<img width="1136" height="710" alt="image" src="https://github.com/user-attachments/assets/7d2b3ce2-ac2a-4cbf-8f96-6d3e3f46df02" />

<img width="1135" height="599" alt="image" src="https://github.com/user-attachments/assets/e3f930be-6a7c-4e1d-a7b8-357b03204d14" />


<img width="1131" height="760" alt="image" src="https://github.com/user-attachments/assets/84062651-18c7-4e36-a002-2e0e813d9f43" />

# RESULT :
• The player starts with a limited number of bullets.




• When the player overlaps with an ammo pickup:




 ○ The ammo is collected.





 
 ○ The player's AmmoCount increases.



 

• The player can now fire additional bullets based on the updated ammo count.
