# Relational-model-Checkpoint

Pour convertir le modèle de relations entre entités en un diagramme relationnel, nous allons définir les tables, les clés primaires et les clés étrangères, ainsi que les relations entre elles. Voici comment cela se présente :

###1. Tables du diagramme relationnel#### Table : Hotel- Hotel_Id (PK)

Hotel_Name
Type_Id (FK vers Type)
Table : Type- Type_Id (PK)
Type_Name
Table : Room- Room_Id (PK)
Floor
Category_Id (FK vers Category)
Hotel_Id (FK vers Hotel)
Table : Category- Category_Id (PK)
Category_Name
Price
Beds_numbers
Table : Employee- Employee_Id (PK)
Employee_Name
Employee_Speciality
Hotel_Id (FK vers Hotel)
###2. Relations- Un Hôtel peut avoir plusieurs Types (relation1:N).

Un Type est associé à un ou plusieurs Hôtels (relation N:1).
Un Hôtel est composé de plusieurs Chambres (relation1:N).
Une Chambre est associée à un Catégorie (relation N:1).
Un Type peut avoir plusieurs Chambres (relation N:1).
Un Catégorie peut être associé à plusieurs Chambres (relation1:N).
Un Hôtel peut avoir plusieurs Employés (relation1:N).
Un Employé travaille dans un Hôtel (relation N:1).
###3. Diagramme relationnel (notation textuelle)

scss
[Hotel]  
 Hotel_Id (PK)  
 Hotel_Name Type_Id (FK)  

[Type]  
 Type_Id (PK)  
 Type_Name[Room]  
 Room_Id (PK)  
 Floor Category_Id (FK)  
 Hotel_Id (FK)  

[Category]  
 Category_Id (PK)  
 Category_Name Price Beds_numbers[Employee]  
 Employee_Id (PK)  
 Employee_Name Employee_Speciality Hotel_Id (FK)  
###4. Clés étrangères- Type_Id dans Hotel est une clé étrangère vers Type.

Category_Id dans Room est une clé étrangère vers Category.
Hotel_Id dans Room est une clé étrangère vers Hotel.
Hotel_Id dans Employee est une clé étrangère vers Hotel.
Cela constitue une représentation claire du modèle de données, permettant de gérer efficacement les informations de l'hôtel, des chambres, des types, des catégories et des employés.
