The inputs are an unseen command and the random objects including items required to execute the command. 

----

* ### Tabletop Output Samples for GPT2-medium
These are outputs of fine-tuned GPT2-medium on our command-steps pairs dataset for tabletop. We aim to apply it on the tabletop simulator, and the possible actions in the tabletop simulator are only pick-and-place, so, we restrict all actions in the tabletop dataset to pick or place. We found that GPT2-medium achieves a higher success rate than GPT3.5 on Socratic Models on the tabletop simulator. If you want more details, please refer to our paper.   

**Note.** GPT2-medium sometimes generate unnecessary extra actions at the end, but the result isn't incorrect. The issue is appears only on tabletop domain. See the output samples below for more details.

<details>
  <summary> Output Samples </summary>
  
  ```
  input=
  "Objects= ['Yellow square block', 'Red square block', 'Yellow bowl', 'Green square block']
  Command= Arrange the square blocks in different corners.
  Action steps= "
  
  output=
  "Step 1. PICK up the RED SQUARE BLOCK. (ACTION: PICK | TARGET: RED SQUARE BLOCK)
  Step 2. PLACE the red square block to the TOP LEFT CORNER of the table. (ACTION: PLACE | TARGET: TOP LEFT CORNER)
  Step 3. PICK up the YELLOW SQUARE BLOCK. (ACTION: PICK | TARGET: YELLOW SQUARE BLOCK)
  Step 4. PLACE the yellow square block to the BOTTOM RIGHT CORNER of the table. (ACTION: PLACE | TARGET: BOTTOM RIGHT CORNER)
  Step 5. PICK up the GREEN SQUARE BLOCK. (ACTION: PICK | TARGET: GREEN SQUARE BLOCK)
  Step 6. PLACE the green square block to the TOP RIGHT CORNER of the table. (ACTION: PLACE | TARGET: TOP RIGHT CORNER) "
  ```
  ```
  input=
  "Objects= ['Yellow crescent block', 'Blue circle block', 'Red circle block', 'Yellow moon block', 'Green circle block']
  Command= Arrange the circle blocks in traffic light order.
  Action steps= "
  
  output=
  "Step 1. PICK up the RED CIRCLE BLOCK. (ACTION: PICK | TARGET: RED CIRCLE BLOCK)
  Step 2. PLACE the red circle block at the BOTTOM of the table. (ACTION: PLACE | TARGET: BOTTOM OF THE TABLE)
  Step 3. PICK up the GREEN CIRCLE BLOCK. (ACTION: PICK | TARGET: GREEN CIRCLE BLOCK)
  Step 4. PLACE the green circle block in the MIDDLE of the table. (ACTION: PLACE | TARGET: MIDDLE OF THE TABLE)
  Step 5. PICK up the BLUE CIRCLE BLOCK. (ACTION: PICK | TARGET: BLUE CIRCLE BLOCK)
  Step 6. PLACE the blue circle block at the TOP of the table. (ACTION: PLACE | TARGET: TOP OF THE TABLE)"
  ```
  ```
  input=
  "Objects= ['Yellow circle block', 'Blue moon block', 'Red circle block', 'Green bowl', 'Green circle block', 'Yellow bowl', 'Red bowl']
  Command= Pick a circle thing and place it in the same colored bowl, in order of red, yellow, and green.
  Action steps= "
  
  output=
  "Step 1. PICK up the RED CIRCLE BLOCK. (ACTION: PICK | TARGET: RED CIRCLE BLOCK)
  Step 2. PLACE the red circle block in the RED BOWL. (ACTION: PLACE | TARGET: RED BOWL)
  Step 3. PICK up the YELLOW CIRCLE BLOCK. (ACTION: PICK | TARGET: YELLOW CIRCLE BLOCK)
  Step 4. PLACE the yellow circle block in the YELLOW BOWL. (ACTION: PLACE | TARGET: YELLOW BOWL)
  Step 5. PICK up the GREEN CIRCLE BLOCK. (ACTION: PICK | TARGET: GREEN CIRCLE BLOCK)
  Step 6. PLACE the green circle block in the GREEN BOWL. (ACTION: PLACE | TARGET: GREEN BOWL)
  Step 7. PICK up the RED CIRCLE BLOCK. (ACTION: PICK | TARGET: RED CIRCLE BLOCK)
  Step 8. PLACE the red circle block in the RED BOWL. (ACTION: PLACE | TARGET: RED BOWL)"

  # The result isn't incorrect, but have unnecessary extra action at the end.
  ```
  ```
  input=
  "Objects= ['Green semicircle block', 'Red circle block', 'Blue semicircle block', 'Green moon block', 'Green circle block']
  Command= Arrange all green blocks in a row.
  Action steps= "
  
  output=
  "Step 1. PICK up the GREEN CIRCLE BLOCK. (ACTION: PICK | TARGET: GREEN CIRCLE BLOCK)
  Step 2. PLACE the green circle block at the START of the ROW. (ACTION: PLACE | TARGET: START of the ROW)
  Step 3. PICK up the GREEN SEMICIRCLE BLOCK. (ACTION: PICK | TARGET: GREEN SEMICIRCLE BLOCK)
  Step 4. PLACE the green semicircle block NEXT TO THE GREEN CIRCLE BLOCK. (ACTION: PLACE | TARGET: NEXT TO THE GREEN CIRCLE BLOCK)
  Step 5. PICK up the GREEN MOON BLOCK. (ACTION: PICK | TARGET: GREEN MOON BLOCK)
  Step 6. PLACE the green moon block NEXT TO THE GREEN SEMICIRCLE BLOCK. (ACTION: PLACE | TARGET: NEXT TO THE GREEN SEMICIRCLE BLOCK)
  Step 7. PICK up the GREEN CIRCLE BLOCK. (ACTION: PICK | TARGET: GREEN CIRCLE BLOCK)
  Step 8. PLACE the green circle block NEXT TO THE GREEN MOON BLOCK. (ACTION: PLACE | TARGET: NEXT TO THE GREEN MOON BLOCK)"

 # The result isn't incorrect, but have unnecessary extra action at the end.
  ```
  ```
  input=
  "Objects= ['Yellow cube', 'Blue pentagon block', 'Red cube', 'Yellow sqaure block', 'Green circle block', 'Green cube']
  Command= Arrange each cubes in each corner.
  Action steps= "
  
  output=
  "Step 1. PICK up the RED CUBE. (ACTION: PICK | TARGET: RED CUBE)
  Step 2. PLACE the red cube to the TOP LEFT CORNER of the table. (ACTION: PLACE | TARGET: TOP LEFT CORNER)
  Step 3. PICK up the YELLOW CUBE. (ACTION: PICK | TARGET: YELLOW CUBE)
  Step 4. PLACE the yellow cube to the TOP RIGHT CORNER of the table. (ACTION: PLACE | TARGET: TOP RIGHT CORNER)
  Step 5. PICK up the GREEN CUBE. (ACTION: PICK | TARGET: GREEN CUBE)
  Step 6. PLACE the green cube to the BOTTOM LEFT CORNER of the table. (ACTION: PLACE | TARGET: BOTTOM LEFT CORNER)"
  ```
  ```
  input=
  "Objects= ['Yellow cube', 'Blue pentagon block', 'Red cube', 'Yellow sqaure block', 'Green circle block', 'Green cube']
  Command= Arrange a yellow cube, red cube, green cube and a blue pentagon block in each corner.
  Action steps= "
  
  output=
  "Step 1. PICK up the YELLOW CUBE. (ACTION: PICK | TARGET: YELLOW CUBE)
  Step 2. PLACE the yellow cube to the TOP LEFT CORNER of the table. (ACTION: PLACE | TARGET: TOP LEFT CORNER)
  Step 3. PICK up the RED CUBE. (ACTION: PICK | TARGET: RED CUBE)
  Step 4. PLACE the red cube to the TOP RIGHT CORNER of the table. (ACTION: PLACE | TARGET: TOP RIGHT CORNER)
  Step 5. PICK up the GREEN CUBE. (ACTION: PICK | TARGET: GREEN CUBE)
  Step 6. PLACE the green cube to the BOTTOM LEFT CORNER of the table. (ACTION: PLACE | TARGET: BOTTOM LEFT CORNER)
  Step 7. PICK up the BLUE PENTAGON BLOCK. (ACTION: PICK | TARGET: BLUE PENTAGON BLOCK)
  Step 8. PLACE the blue pentagon block to the BOTTOM RIGHT CORNER of the table. (ACTION: PLACE | TARGET: BOTTOM RIGHT CORNER)"
  ```

</details>   

----

* ### Kitchen Output Samples for GPT2-medium
These are outputs of fine-tuned GPT2-medium on our command-steps pairs dataset for kitchen. we constrain the possible actions to pick, place, move, and utilize the objects. We conducted a survey, to evaluate whether small LMs finetuned on our datasets can plan effectively for high-level commands as LLMs. As a result, there is little difference in heuristic scores between GPT2-medium and GPT3.5, and even GPT2-medium scored more consistently higher.
<details>
  <summary> Output Samples </summary>
  
  ```
  input=
  
  output=
  ```

</details>

----
