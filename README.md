# Data Analysis using Excel
Data Analysis Project for Accenture NA on Forage.
## Project Details:
### Scenario:
Lets say, a Social Media Company is having trouble identifying which content on there platform is popular, due to the enormous amount of data being generated. They have given me the **csv files** containing Data regarding the following
#### User
ID: Unique ID of the user (automatically generated)

Name: Full name of user

Email: Email address of user
#### Profile
User ID: Unique ID of a user that exists in the User table

Interests: Interests of the associated user

Age: Age of the associated user
#### Location
User ID: Unique ID of a user that exists in the User table

Address: Full address of the user
#### Session
User ID: Unique ID of a user that exists in the User table

Device: Mobile device that they used for this session on the application

Duration: Amount of time in minutes that this user stayed active on the application during this session
#### Content
ID: Unique ID of the content that was uploaded (automatically generated)

User ID: Unique ID of a user that exists in the User table

Type: A string detailing the type of content that was uploaded

Category: A string detailing the category that this content is relevant to

URL: Link to the location where this content is stored
#### Reaction
Content ID: Unique ID of a piece of content that was uploaded

User ID: Unique ID of a user that exists in the User table who reacted to this piece of content

Type: A string detailing the type of reaction this user gave

Datetime: The date and time of this reaction
#### ReactionTypes
Type: A string detailing the type of reaction this user gave

Sentiment: A string detailing whether this type of reaction is considered as positive, negative or neutral

Score: This is a number calculated by Social Buzz that quantifies how “popular” each reaction is. A reaction type with a higher score
should be considered as a more popular reaction
### Objective:
To find the "Top 5 categories with the largest popularity".

## Implementation:

By looking at the Data, we can conclude the following Data Types to process:
- **String**    - Sequence of characters, digits, or symbols—always treated as text
- **UUID**      - Universally Unique Identifiers
- **Array**     - List with a number of elements in a specific order—typically of the same type
- **Integer**   - Numeric data type for numbers without fractions
- **Timestamp** - Number of seconds that have elapsed since midnight (00:00:00 UTC)
### Data Sets:
The Three Data Sets that we need to have in order to solve the problem are
1. Content
2. Reations
3. ReactionTypes

**Refer** -> [**Given Data**](https://github.com/Imranian/Data-Analysis-using-Excel/tree/main/Given%20Data)
### Schema:

<p align="center">
    <img src="https://github.com/Imranian/Data-Analysis-using-Excel/blob/main/Schema.png">
</p>

### Approach:
#### Step 1: Requirement gathering
- client wanted to see “An analysis of their content categories showing the top 5 categories with the largest popularity”.
- Popularity is quantified by the “Score” given to each reaction type.
- We therefore need data showing the content ID, category, content type, reaction type, and reaction score.
- So, to figure out popularity, we’ll have to add up which content categories have the largest score.
#### Step 2: Data Cleaning
Clean the data by:
- removing rows that have values which are missing,
- changing the data type of some values within a column, and removing columns which are not relevant to this task.
#### Step 3: Data Modelling
Now we want to figure out the top 5 categories. To complete your data modelling, follow these steps:
1. Create a final data set by merging your three tables together

- Use the Reaction table as your base table, then first join the relevant columns from your Content data set, and then the Reaction Types data set.
- Note: You can use a “VLookUp” formula

2. Figure out the Top 5 performing categories

- Add up the total scores for each category.
- Note: You can use the “Sum If” formula
## Result:

<p align="center">
    <img src="https://github.com/Imranian/Data-Analysis-using-Excel/blob/main/My/Top%205.png">
</p>

