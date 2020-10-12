# Election_Analysis
Analysis of Election Results 
## Project Overview
A Colorado Board of Elections employee has given me the following tasks to complete the election audit of a recent local congressional election. 

1. Calculate the total number of votes cast. 
2. Get a complete list of candidates who received votes. 
3. Calculate the total number of votes each candidate received. 
4. Calculate the percentage of votes each candidate won. 
5. Determine the winner of the election based on popular vote. 

## Resources
- Date Source: election_results.csv
- Software: Python 3.7, Visual Studio Code, 1.50.0

## Summary
The analysis of the election show that:
- There were 369,711 votes cast in the election. 

- The candidates were:
  - Diana DeGette
  - Charles Casper Stockham
  - Raymon Anthony Doane
  
- The candidate results were:
  - Charles Casper Stockham received 23% of the vote and 85,213 number of votes.
  - Diana DeGette received 73.8% of the vote and 272,892 number of votes. 
  - Raymon Anthony Doane received 3.1% of the votes and 11,606 number of votes. 
  
- The winner of the election was:
   -Diana DeGette, who received 73.8% of the vote and 272,892 number of votes.
   
 ## Challenge Overview

## Election-Audit Results:
There was a total of 369,711 votes cast in this congressional election.  Sample of code used to obtain total votes was:        
 #Add to the total vote count
 
        total_votes = total_votes + 1
        
•	Breakdown of votes by county
| County | Percentage of Votes | Total # of Votes |
| :---: | :---: | :---|
| Jefferson	| 10.5%	| 38,855 |
|Denver	| 82.8% | 306,055 |
| Arapahoe | 6.7%	| 24,801 |

The following excerpt from the code was used to obtain the number of votes by county and as well as candidate votes with a simple modification of the keywords used for county vs candidate. 

if county_name not in counties:

            #Add the existing county to the list of counties
            
           counties.append(county_name)
           
            #Begin tracking the county's vote count.
            
            county_votes[county_name] = 0
            
   #Add a vote to that county's vote count.
   
            county_votes[county_name] += 1
            
•	Denver had the largest number of votes at 306,055.

•	Breakdown of votes each candidate received:
| Candidate| Percentage of Votes| Total # of Votes |
| :---: | :---: | :---|
| Charles Casper Stockham	| 23%	                | 85,213           |
| Diana DeGette	          | 73.8%	              | 272,892          |
| Raymon Anthony Doane    |   3.1%	            | 11,606           |

•	Diana DeGette won the election with 272,892 votes, which was 73.8% of the total votes tallied by all counties. 

The following is an example of the code used to obtain the percentage of votes from each county.
#Retrieve the county vote count.

county_count = county_votes.get(county)

#Calculate the percent of total votes for the county.

county_percentage = float(county_count) / float(total_votes) * 100

county_results = (f"{county_name}: {county_percentage:.1f}% ({county_count:,})\n")

#Print the county results to the terminal.

print(county_results)

#Save the county votes to a text file.

txt_file.write(county_results)

#Write a decision statement to determine the winning county and get its vote count.

if (county_count > largest_votes):

largest_votes = county_count

largest_turnout = county

## Challenge Summary
## Election-Audit Summary:

The script that was utilized to complete the analysis of this specific congressional precinct could be modified for use with multiple elections. For example, with slight modifications the data could be used to analyze age or gender of voters and how those voters voted for each candidate. This script could also be  slightly modified to include analysis of statewide or country elections with modification to the keywords that were used, while keeping the formatting of the script.

 
