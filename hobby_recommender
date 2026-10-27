# Fact definition class
# H(x, l, c, s, b, t) --> x is a hobby in l location, of c category, with s social preference, 
# requires b budget and t preference of technology 
class Hobby:
    """
    - Constructor -
    name: the name of the hobby/hobbies which the system will recommend
    location: indoor or outdoor
    category: active/sport or calm
    social_preference: alone or in a group
    budget: low or high
    is_tech: likes tech/brain teaser activities or not (T/F)

    """
    def __init__(self, name, location, category, social_preference, budget, is_tech):
        self.name = name
        self.location = location
        self.category = category
        self.social_preference = social_preference
        self.budget = budget
        self.is_tech = is_tech
    
# Writing facts: Create a list of hobbies using Hobby class
hobbies = [ 
    # Indoor - calm - social - low - tech
    Hobby("Strategy board games - Joining coding hackathons", "indoor", "calm", "social", "low", True),
    # Indoor - calm - social - low
    Hobby("Book Clubs - Meditation Classes - Art Therapy - Writing Workshops", "indoor", "calm", "social", "low", False), 
    # Indoor - calm - social - high - tech
    Hobby("Virtual Reality Art Exhibitions - Online Coding Collaborations - Virtual Book Discussions", "indoor", "calm", "social", "high", True), 
    # Indoor - calm - social - high 
    Hobby("Spa Sessions - Private Art Classes - Exclusive Book Clubs - Gourmet Cooking Classes", "indoor", "calm", "social", "high", False), 
    # Indoor - calm - alone - low - tech
    Hobby("Sudoku - Free Coding Courses - Mobile Puzzle Games - Crossword Puzzles", "indoor" , "calm" , "alone" , "low", True),
    # Indoor - calm - alone - low 
    Hobby("Painting/Sketching - Candle making - Baking - Reading and writing", "indoor", "calm", "alone", "low", False),
    # Indoor - calm - alone - high - tech
    Hobby("Advanced Coding Projects - Digital Art Creation", "indoor", "calm", "alone", "high", True), 
    # Indoor - calm - alone - high
    Hobby("Oil Painting - Classical Music Composing - Writing - Reading", "indoor", "calm", "alone", "high", False), 
    # Indoor - active - social - low - tech
    Hobby("VR Activities - Interactive Workout Classes", "indoor", "active", "social", "low", True), 
    # Indoor - active - social - low
    Hobby("Home Yoga Sessions - Group Aerobics - Dance Circles - Indoor Team Sports", "indoor", "active", "social", "low", False), 
    # Indoor - active - social - high - tech
    Hobby("VR Fitness Competitions - Smart Gym Workouts - Interactive Dance Simulators - Motion Capture Sports Games", "indoor", "active", "social", "high", True),
    # Indoor - active - social - high 
    Hobby("Dance Classes - VR Fitness Games - Martial Arts Classes" , "indoor" , "active" , "social" , "high" , False),
    # Indoor - active - alone - low - tech
    Hobby("Home workout apps - VR fitness games", "indoor", "active", "alone", "low", True),
    # Indoor - active - alone - low
    Hobby("Bodyweight exercises - Skipping rope", "indoor", "active", "alone", "low", False),
    # Indoor - active - alone - high - tech
    Hobby("Smart gym equipment - VR sports simulations", "indoor", "active", "alone", "high", True),
    # Indoor - active - alone - high 
    Hobby("Personal gym setup - Indoor rock climbing", "indoor", "active", "alone", "high", False),
    # Outdoor - calm - social - low - tech 
    Hobby("Obesrvation and data collection in a group - Nature videography with social sharing", "outdoor", "calm", "social", "low",True),
    # Outdoor - calm - social - low 
    Hobby("Picinc with the family - Camping", "outdoor", "calm", "social", "low",False),
    # Outdoor - calm - social - high - tech 
    Hobby("Drone photography - Rideing electric bikes", "outdoor", "calm", "social", "high",True),
    # Outdoor - calm - social - high 
    Hobby("Painting with a group of artists", "outdoor", "calm", "social", "high",False),
    # Outdoor - calm - alone - low - tech 
    Hobby("Photography - Digital drawing", "outdoor", "calm", "alone", "low",True),
    # Outdoor - calm - alone - low 
    Hobby("Yoga - Gardening - Fishing - Landscape photography", "outdoor", "calm", "alone", "low",False),
    # Outdoor - calm - alone - high - tech 
    Hobby("Wildlife filmmaking - Professional photography - Stargazing with a telescope", "outdoor", "calm", "alone", "high", True),
    # Outdoor - calm - alone - high 
    Hobby("Travelling - Visiting exhibits - smart gardening", "outdoor", "calm", "alone", "high", False),
    # Outdoor - active - social - low - tech 
    Hobby("Playing GPS-Based AR Games", "outdoor", "active", "social", "low", True),
    # Outdoor - active - social - low
    Hobby("Soccer - Jogging - Cycling ", "outdoor", "active", "social", "low",False),
    # Outdoor - active - social - high - tech 
    Hobby("Drone flying - E-biking with a group", "outdoor", "active", "social", "high", True),
    # Outdoor - active - social - high 
    Hobby("Camping - Surfing - Horseback Riding - Golf", "outdoor", "active", "social", "high",False),
  # Outdoor - active - alone - low - tech
    Hobby("Drone racing", "outdoor", "active", "alone", "low", True),
    # Outdoor - active - alone - low
    Hobby("Jogging - Solo cycling", "outdoor", "active", "alone", "low", False),
    # Outdoor - active - alone - high - tech
    Hobby("Electric skateboarding - GPS-guided hiking", "outdoor", "active", "alone", "high", True),
    # Outdoor - active - alone - high
    Hobby("Scuba diving - Solo kayaking", "outdoor", "active", "alone", "high", False),
]

# Write the rule
def recommend_hobby(location, category, social_preference, budget, is_tech):
    # Check for every hobby in the list
    for hobby in hobbies: 
        # if the hobby location is the same as user's input
        if hobby.location == location:
            # if the hobby category is the same as user's input
            if hobby.category == category:
                # if the hobby social preference is the same as user's input
                if hobby.social_preference == social_preference:
                    # if the hobby budget is the same as user's input
                    if hobby.budget == budget:
                        # if the hobby specified tech preference is the same as user's input
                        if hobby.is_tech == is_tech:
                            # return the hobbies defined in the list
                            return f"The recommended hobbies for your intersets are: {hobby.name}" 
                        
# Function to process the queries. The parameters are initialized to - (blank) and will change according to 
# the user input
def query_hobby(location = "-", category = "-", social_preference = "-", budget = "-", is_tech = "-"):
    # Initialize the results to include all hobbies
    results = hobbies
    # Dictionary to store parameters of the query, it is initially blank (includes all possibilites)
    query_parameters = {"location" : ["_"], "category" : ["_"], "social_preference" : ["_"], "budget" : ["_"], "tech" : ["_"]}
    # If the location is not blank, then limit the results to that location and add it as a parameter
    if location != "-" :
        results = [hobby for hobby in results if hobby.location == location]
        query_parameters["location"][0] = location
    # If the category is not blank, then limit the results to that category and add it as a parameter
    if category != "-" :
        results = [hobby for hobby in results if hobby.category == category]
        query_parameters["category"][0] = category
    # If the social_preference is not blank, then limit the results to that social_preference and add it as a parameter
    if social_preference != "-" :
        results = [hobby for hobby in results if hobby.social_preference == social_preference]
        query_parameters["social_preference"][0] = social_preference
    # If the budget is not blank, then limit the results to that budget and add it as a parameter
    if budget != "-" :
        results = [hobby for hobby in results if hobby.budget == budget]
        query_parameters["budget"][0] = budget
    # If the tech preference is not blank, then limit the results to that tech preference and add it as a parameter
    if is_tech != "-" :
        results = [hobby for hobby in results if hobby.is_tech == (is_tech == "yes")]
        query_parameters["tech"][0] = is_tech
    
    # Finally print the query and the results
    print(f'The query : Hobby(hobby, {query_parameters["location"][0]}, {query_parameters["category"][0]}, {query_parameters["social_preference"][0]}, {query_parameters["budget"][0]}, {query_parameters["tech"][0]}) results:')
    for result in results:
        print(result.name)
    
                            
# Function to get and validate user input 
def get_valid_input(prompt, valid_options):  
    # loop to make sure the user input is correct
    while True:  
        # lower() converts input into lowercase and strip() removes extra spaces
        user_input = input(prompt).strip().lower() 
        # Check if input is valid
        if user_input in valid_options: 
            return user_input
        # Display error message with correct options 
        print(f"Invalid input. Please choose from: {', '.join(valid_options)}")  

# Function to give prompts to the user
def get_input():
    # Welcome message, and ask the user to choose from the menu
    choice = int(get_valid_input("Welcome dear user. Choose one of the following: \n1. Get hobby recommendations\n2.Query hobbies\n3.Quit\nYour choice: ", ["1", "2", "3"]))
    
    while(choice != 3):
            if (choice == 1):
                # Ask questions for each one of the criteria and get user input
                print("Answer the following questions to get recommendations which best match your interests:")
                location = get_valid_input("1. Do you prefer indoor or outdoor activities? (answer indoor/outdoor) ", ["indoor", "outdoor"])  
                category = get_valid_input("2. Do you prefer active hobbies like sports or calm hobbies like art? (answer active/calm) ", ["active", "calm"]) 
                social = get_valid_input("3. Do you prefer spending time alone or with a group of people? (answer alone/social) ", ["alone", "social"]) 
                budget = get_valid_input("4. What is the budget you can spend on a hobby? (answer low/high) ", ["low", "high"]) 
                tech = get_valid_input("5. Are you interested in tech and brain teasers (puzzles, problem-solving, etc.)? (answer yes/no) ", ["yes", "no"])  

                # Call recommend_hobby() to give recommendations based on users input
                # tech == "yes" will return true or false depending if the user likes hobbies involoving technology or not
                recommendation = recommend_hobby(location, category, social, budget, tech == "yes")
                # Finally print the recommendation to the user
                print(recommendation)
                # Print the prompt again to process user's choice
                choice = int(get_valid_input("Choose one of the following: \n1. Get hobby recommendations\n2.Query hobbies\n3.Quit\nYour choice: ", ["1", "2", "3"]))
                
            elif (choice == 2):
                # If the user choose query, ask to give parameters to form the query
                location = get_valid_input("Enter your query parameter: indoor/outdoor or - to leave it blank:  ", ["indoor", "outdoor", "-"])
                category = get_valid_input("Enter your query parameter: calm/active or - to leave it blank:  ", ["active", "calm", "-"])
                social = get_valid_input("Enter your query parameter: alone/social or - to leave it blank:  ", ["alone", "social", "-"])
                budget = get_valid_input("Enter your query parameter: low/high or - to leave it blank:  ", ["low", "high", "-"])
                tech = get_valid_input("Enter your query parameter: yes/no or - to leave it blank (yes means you prefer tech hobbies):  ", ["yes", "no", "-"])
                # Call the function to process the query results
                query_hobby(location, category, social, budget, tech)
                # Print the prompt again to process user's choice
                choice = int(get_valid_input("Choose one of the following: \n1. Get hobby recommendations\n2.Query hobbies\n3.Quit\nYour choice: ", ["1", "2", "3"]))


# Main function
if __name__ == '__main__':
    # Call the function to get input from the user
    get_input()
    
