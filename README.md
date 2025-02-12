# Mod2 Week2 Assessment - <Eli Paris>

## Setup
1. Fork this repository.
1. Add ONE of the following GitHub profiles as a collaborator to your forked repo:
`memcmahon`, `rtillies`, `zoefarrell`
1. Clone your repo to your local machine.
1. Open your cloned repository in Visual Studio.
1. Insert your name on line 1 to replace `<YOUR NAME HERE>` above.

## Questions (10 Points Possible)
**Important** Answer these questions in this file on your `main` branch.  When finished with the questions, commit and push your main branch.  You do not need to create a pull request yet!

1. What does TDD stand for?
TDD stand for Test Driven Development and is the process of writing tests BEFORE the code

1. What are three benefits of using TDD?
    1.TDD forces the developer to really think about what they want the code to look like
    2.It also allows the devloper to break down problems easier than just writing the code outright with out knowing what the program might look like
    3.This also forces the developer to only write the code that they need and helps to prevent going down unproductive trains of thought when writing code

1. Imagine you are in an interview.  The interviewer asks: How do you use TDD? How would you answer?
    With my skills in test driven development I would write tests for a baseline for how I am invisioning the main code to look like. This will allow me to focus more clearly on what needs to be down and gain a better visual picture of how a the code might look like. Likewise, when the code is written I can fo forward with confidence that the code works when I try refeactoring or implementing new features.

1. For the class below, outline the tests you would need.  Try to use as much C# syntax as possible. The first test has been provided for you. (this question is worth 4 points)
```c#
public class Dog
    {
        public string Name { get; }
        public string Breed { get; }
        public bool IsHungry { get; private set; }

        public Dog(string name, string breed)
        {
            Name = name;
            Breed = breed;
            IsHungry = true;
        }

        public void Eat()
        {
            IsHungry = false;
        }

        public void Sleep()
        {
            IsHungry = true;
        }

        public string Speak()
        {
            return "Bark Bark!";
        }
    }
```
```c#
// Add your tests here

[Fact]
public void DogHasNameAttribute()
{
    Dog dog1 = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Nile", dog.Name);
    Assert.Equal("Golden Retriever", dog1.Breed);
}

[Fact]
public void EatMethodMakesIsHungryFalse ()
{
    Dog dog1 = new Dog("Nile", "Golden Retriever");

    dog1.Eat();

    Assert.False(dog1.IsHungry);
    //or
    Assert.Equal(false, dog1.IsHungry);

}

[Fact]
public void SleepMethodMakesIsHungryTrue()
{
    Dog dog1 = new Dog("Nile", "Golden Retriever");
    
    dog1.Sleep();

    Assert.True(dog1.IsHungry);
    //or
    Assert.Equal(true, dog1.IsHungry);
}

[Fact]
public void SleepMethodReturnsString()
{
    Dog dog1 = new Dog("Nile", "Golden Retriever");
    
    string bark = dog1.Speak();

    Assert.Equal("Bark Bark!", bark);

}

```

5. What is a merge conflict, and when might you encounter one?
    A merge conflict can happen when you try to merge branchs into one another. This is caused by code exsisting in the same place on both branches.
1. You and a partner are working on a project together.  Your partner is working on aa-branch; you are working on bb-branch.  In as much detail as possible, describe how you both would get your work combined onto the main branch.
    I would first commit and push up my code to github and make a pullrequest from the branch i was working on to the main branch. this will allow my partner to review my code and "ask" for approvel to merge it. my partner would do the same thing i just desribed but for their branch. I now have a pull request to review and potenially approve. if we both find that code can be merged into the main branch one or both of us might run into a merge conflict if we wrote code in the same spot
1. Why is it good practice to have someone else approve and/or merge your PR?
    Its good practice because communcation is key when working on a team. Merging your own branch has more potential to create problems for your team when trying to implement their code. It is vitial to get another set of eyes on your code to avoid communcation errors as much as possible.
  
**Before moving on to the next section, commit your work and push your main branch!**
  
## Git Exercise (6 points possible)

1. Create a new branch called `elephants` (1 point)

1. Add the following to the end of the Animal Tracker file:

```
Elephants
- African Savanna
- Asian
- African Forest
```

3. Commit this change to the Animal Tracker file with an appropriate message. (1 point)

1. Create the following files with the listed contents:

**African Savanna.txt**
```
Average shoulder height: 2.6-3.2 meters
Average mass: 3.3-6.6 short tons
```

**Asian Elephant.txt**
```
Average shoulder height: 2.4-2.8 meters
Average mass: 3.0-4.4 short tons
```

**African Forest Elephant.txt**
```
Average shoulder height: 1.8-3.0 meters
Average mass: 2,000-7,000 kilograms
```

5. Add and Commit these new files with an appropriate message. (1 point)

1. Push your `elephants` branch to GitHub. (1 point)

1. Create a Pull Request in GitHub. Write a short description of the changes you made to the repo. (1 point) 

1. Request a review from your collaborator. (1 point)
  
## Submission

Submit the Assessment Submission form linked in your cohort slack channel!

## Rubric

This assessment has a total of 16 Points. Earning 11 or more points is a pass and will indicate that you are progressing well with the material.

As a reminder, this assessment is for students and instructors to determine if there are any areas that need additional reinforcement!
