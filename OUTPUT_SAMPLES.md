Output samples
----

These are input-output samples for GPT2-medium on tabletop and kitchen domain. The inputs are an unseen command and the random objects including items required to execute the command. The outputs are action steps to execute the input command. If you want more details, please refer to our paper.
 
----

* ### Tabletop Output Samples for GPT2-medium
These are outputs of fine-tuned GPT2-medium on our command-steps pairs dataset for tabletop. We aim to apply it on the tabletop simulator, and the possible actions in the tabletop simulator are only pick-and-place, so, we restrict all actions in the tabletop dataset to pick or place. We found that GPT2-medium achieves a higher success rate than GPT3.5 on Socratic Models on the tabletop simulator.

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
These are outputs of fine-tuned GPT2-medium on our command-steps pairs dataset for kitchen. We constrain the possible actions to pick, place, move, and utilize the objects. We conducted a survey, to evaluate whether small LMs finetuned on our datasets can plan effectively for high-level commands as LLMs. As a result, we found that there is little difference in scores between GPT2-medium and GPT3.5, and even GPT2-medium scored more consistently higher. The output samples below are samples used in the survey.

<details>
  <summary> Output Samples </summary>
  
  ```
  input= 
  "Objects= [ 'Fry pan', 'Tea towel', 'Teapot', 'Potato' ]
  Command= Clean a fry pan with a tea towel.
  Action steps="
  
  output=
  "Step 1. PICK up the tea towel. (ACTION: Pick | TARGET: Tea towel)
  Step 2. MOVE to the fry pan. (ACTION: Move | TARGET: Fry pan)
  Step 3. CLEAN the fry pan with the tea towel. (ACTION: Clean | TARGET: Tea towel, Fry pan)"
  ```
  ```
  input= 
  "Objects= ['Bread', 'Spoon', 'Cookie dough', 'Bacon', 'Jam', 'Egg', 'Cheese', 'Fry pan']
  Command= Make a sandwich with bacon and egg.
  Action steps="
  
  output=
  "Step 1. PICK up two slices of bread. (ACTION: Pick | TARGET: Bread)
  Step 2. SPREAD jam on one slice of bread. (ACTION: Spread | TARGET: Jam, On one slice of bread)
  Step 3. PLACE a slice of bacon on the other slice of bread. (ACTION: Place | TARGET: Slice of bacon, On the other slice of bread)
  Step 4. STACK the egg into the pan. (ACTION: Stack | TARGET: Egg, Into the pan)
  Step 5. COOK the bacon and egg in the pan. (ACTION: Cook | TARGET: Bacon, Egg, In the pan)
  Step 6. PICK up the cooked bacon and egg. (ACTION: Pick | TARGET: Cooked bacon and egg)
  Step 7. PLACE the cooked bacon and egg on one slice of bread. (ACTION: Place | TARGET: Cooked bacon and egg, On one slice of bread)
  Step 8. PICK up the other slice of bread. (ACTION: Pick | TARGET: Other slice of bread)
  Step 9. PLACE the other slice of bread on top of the bacon and egg. (ACTION: Place | TARGET: Other slice of bread, On top of the bacon and egg)"
  ```
  ```
  input= 
  "Objects= ['Cookie', 'Cloth', 'Table', 'Knife', 'Sink']
  Command= Wipe up water around the sink.
  Action steps="
  
  output=
  "Step 1. PICK up a cloth. (ACTION: Pick | TARGET: Cloth)
  Step 2. MOVE to the sink. (ACTION: Move | TARGET: Sink)
  Step 3. TURN ON the faucet. (ACTION: Turn on | TARGET: Faucet)
  Step 4. WET the cloth under the running water. (ACTION: Wet | TARGET: Cloth, Running water)
  Step 5. TURN OFF the faucet. (ACTION: Turn off | TARGET: Faucet) 
  Step 6. WRING OUT the excess water from the cloth. (ACTION: Wring out | TARGET: Cloth) 
  Step 7. MOVE to the table. (ACTION: Move | TARGET: Table) 
  Step 8. WIPE down the table with the damp cloth. (ACTION: Wipe | TARGET: Damp cloth, Table)"
  ```
  ```
  input= 
  "Objects= ['Fry pan', 'Teapot', 'Cookie dough', 'Potato', 'Knife', 'Lemon'] 
  Command= Pour lemon juice into the tea pot.
  Action steps="
  
  output=
  "Step 1. PICK up the lemon. (ACTION: Pick | TARGET: Lemon)
  Step 2. CUT the lemon in half using a knife. (ACTION: Cut | TARGET: Knife, Lemon)
  Step 3. PICK up the lemon halves. (ACTION: Pick | TARGET: Lemon halves)
  Step 4. MOVE to the teapot. (ACTION: Move | TARGET: Teapot)
  Step 5. SQUEEZE the lemon halves into the teapot. (ACTION: Squeeze | TARGET: Lemon halves, Teapot)"
  ```
  ```
  input= 
  "Objects= ['Cucumber', 'Lettuce', 'Tray', 'Sink', 'Knife', 'Cup']
  Command= Slice the washed lettuce and place it on tray.
  Action steps="

  output=
  "Step 1. PICK up the lettuce. (ACTION: Pick | TARGET: Lettuce)
  Step 2. MOVE to the sink. (ACTION: Move | TARGET: Sink)
  Step 3. WASH the lettuce under running water. (ACTION: Wash | TARGET: Lettuce)
  Step 4. PICK up the knife. (ACTION: Pick | TARGET: Knife)
  Step 5. SLICE the lettuce using the knife. (ACTION: Slice | TARGET: Knife, Lettuce)
  Step 6. PLACE the sliced lettuce on the tray. (ACTION: Place | TARGET: Sliced lettuce, On the tray)"
  ```
  ```
  input= 
  "Objects= ['Coffee machine', 'Bread', 'Plate', 'Cookies', 'Table', 'Cup', 'Sink']
  Command= Set up a cup of coffee and cookies.
  Action steps="
  
  output=
  "Step 1. PICK up a cup. (ACTION: Pick | TARGET: Cup)
  Step 2. MOVE to the coffee machine. (ACTION: Move | TARGET: Coffee machine)
  Step 3. PLACE the cup under the coffee machine. (ACTION: Place | TARGET: Cup, Under the coffee machine)
  Step 4. PRESS the button to fill the cup with coffee. (ACTION: Press | TARGET: Button, Cup)
  Step 5. PICK up the cookies. (ACTION: Pick | TARGET: Cookies)
  Step 6. MOVE to the table. (ACTION: Move | TARGET: Table)
  Step 7. PLACE the cookies on a plate on the table. (ACTION: Place | TARGET: Cookies, On a plate, On the table)"
  ```
  ```
  input= 
  "Objects= ['Fry pan', 'Teapot', 'Cookie dough', 'Potato', 'Jar', 'Lemon juice']
  Command= Pour lemon juice into the tea pot.
  Action steps="
  
  output=
  "Step 1. PICK up the lemon juice. (ACTION: Pick | TARGET: Lemon juice)
  Step 2. PICK up the teapot. (ACTION: Pick | TARGET: Teapot)
  Step 3. POUR the lemon juice into the teapot. (ACTION: Pour | TARGET: Lemon juice, Teapot)"
  ```
  ```
  input= 
  "Objects= ['Oven', 'Tea towel', 'Cookie dough', 'Potato', 'Rolling pin', 'Cookie cutter']
  Command= Bake cookies.
  Action steps="
  
  output=
  "Step 1. PICK up the cookie dough. (ACTION: Pick | TARGET: Cookie dough)
  Step 2. ROLL out the cookie dough using a rolling pin. (ACTION: Roll | TARGET: Cookie dough, Rolling pin)
  Step 3. PICK up the cookie cutter. (ACTION: Pick | TARGET: Cookie cutter)
  Step 4. PRESS the cookie cutter into the rolled out dough. (ACTION: Press | TARGET: Cookie cutter, Rolled out dough)
  Step 5. CAREFULLY REMOVE the excess dough around the cut cookies. (ACTION: Remove | TARGET: Excess dough, Cut cookies)
  Step 6. PLACE the cookie dough into the oven to bake. (ACTION: Place | TARGET: Cookie dough, Oven)"
  ```
  ```
  input= 
  "Objects= ['Cucumber', 'Sink', 'Knife', 'Pumpkin', 'Lettuce', 'Salad bowl', 'Fork']
  Command= Make a salad with lettuce and cucumbers.
  Action steps="
  
  output=
  "Step 1. PICK up the lettuce. (ACTION: Pick | TARGET: Lettuce)
  Step 2. WASH the lettuce under running water. (ACTION: Wash | TARGET: Lettuce)
  Step 3. CHOP the lettuce into bite-sized pieces. (ACTION: Chop | TARGET: Lettuce)
  Step 4. PLACE the chopped lettuce in a salad bowl. (ACTION: Place | TARGET: Chopped lettuce, Salad bowl)
  Step 5. PICK up the cucumber. (ACTION: Pick | TARGET: Cucumber)
  Step 6. SLICE the cucumber into thin pieces. (ACTION: Slice | TARGET: Cucumber)
  Step 7. ADD the sliced cucumber to the salad bowl. (ACTION: Add | TARGET: Sliced cucumber, Salad bowl)
  Step 8. GENTLY TOSS the salad. (ACTION: Gently toss | TARGET: Salad)"
  ```

</details>

----
