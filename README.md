# sorting_hats
print("There are 4 houses:")
print("🦁 Gryffindor")
print("🦅 Ravenclaw")
print("🦡 Hufflepuff")
print("🐍 Slytherin\n")

print("Answer the questions and get sorted into one of the houses!\n")

# Initialize points
gryffindor = 0
ravenclaw = 0
hufflepuff = 0 
slytherin = 0

# Question 1
print("Q1) Do you like Dawn or Dusk?")
print("1) Dawn")
print("2) Dusk")

answer = int(input("Choose 1 or 2: "))
if answer == 1:
  gryffindor += 1
  ravenclaw += 1
elif answer == 2:
  hufflepuff += 1
  slytherin += 1
else:
  print("Invalid input!\n")

# Question 2
print("\nQ2) When I’m dead, I want people to remember me as:")
print("1) The Good")
print("2) The Great")    
print("3) The Wise")
print("4) The Bold")

answer_2 = int(input("Choose 1-4: "))
if answer_2 == 1:
  hufflepuff += 2
elif answer_2 == 2:
  slytherin += 2
elif answer_2 == 3:
  ravenclaw += 2
elif answer_2 == 4:
  gryffindor += 2
else:
  print("Invalid input!\n")

# Question 3
print("\nQ3) Which kind of instrument most pleases your ear?")      
print("1) The Violin")      
print("2) The Trumpet")      
print("3) The Piano")      
print("4) The Drum") 

answer_3 = int(input("Choose 1-4: "))

if answer_3 == 1:
  slytherin += 4
elif answer_3 == 2:
  hufflepuff += 4
elif answer_3 == 3:
  ravenclaw += 4
elif answer_3 == 4:
  gryffindor += 4
else:
  print("Invalid input!\n")

# Final Result
# Dictionary to store scores
houses = {
    "Gryffindor": gryffindor,
    "Ravenclaw": ravenclaw,
    "Hufflepuff": hufflepuff,
    "Slytherin": slytherin
}

# Find the house with the highest score
selected_house = max(houses, key=houses.get)

# Print result
print("\n🪄 The Sorting Hat has made its decision...")
print(f"🎉 You have been sorted into: {selected_house}!")

# Optional: Show scores
print("\nHouse Scores:")
for house, score in houses.items():
    print(f"{house}: {score}")
