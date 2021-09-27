--count the number of teams
select COUNT() 
from Team;

--top 5 man of the match 
select p.Player_Name,COUNT(m.Match_Id) 
from "Match" m,Player p 
where m.Man_of_the_Match = p.Player_Id 
group by p.Player_Name 
order by COUNT(m.Match_Id) DESC
limit 5;


--number of toss won with respect to teams 
select t.Team_Name, COUNT(m.Toss_Winner) 
from Team t , "Match" m
where t.Team_Id = m.Toss_Winner
group by t.Team_Name 
order by COUNT(m.Toss_Winner) DESC ;

--details of team choose batting when toss won
SELECT t.Team_Name,COUNT(m.Match_Id) 
from "Match" m , Team t  
where m.Toss_Winner = t.Team_Id and m.Toss_Decide = 2
group by t.Team_Name 
order by COUNT(m.Match_Id) DESC ;

--number of wons who choose batting first
SELECT t.Team_Name , COUNT(m.Match_Id) 
from "Match" m, Team t 
where m.Match_Winner = t.Team_Id and m.Toss_Decide = 2 
group by t.Team_Name ;

--number of match played in each season with year
select COUNT( m.Match_Id) as count, s.Season_Id, s.Season_Year  
from "Match" m , Season s, Team t 
where m.Season_Id = s.Season_Id 
group by s.Season_Id 
order by s.Season_Year ;

--number of match played in each city
select v.City_Id, c.City_Name, count(m.Venue_Id)
from City c,"Match" m 
inner join Venue v on v.City_Id = c.City_Id
where m.Venue_Id = v.Venue_Id 
group by c.City_Name 
order by COUNT( m.Match_Id) DESC ;

--number of times a team win both toss and match 
select count( m.Match_Id), m.Match_Winner 
from "Match" m
WHERE m.Toss_Winner = m.Match_Winner
group by m.Match_Winner ;


--top 10 venue where most matches played
 select COUNT(m.Match_Id), m.Venue_Id, v.Venue_Name 
 from "Match" m,Venue v 
 where m.Venue_Id = v.Venue_Id 
 group by m.Venue_Id 
order by COUNT(m.Match_Id) DESC
limit 10;

--nnumber of matches played by each Team
SELECT m.Match_Id, m.Team_1, t.Team_Name
from "Match" m, Team t 
where m.Team_1 = t.Team_Id 
union
select m.Match_Id, m.Team_2, t.Team_Name
from "Match" m, Team t
where m.Team_2 = t.Team_Id
group by t.Team_Name
;


--which team won by run type
select COUNT( m.Match_Id),m.Match_Winner 
from "Match" m,Team t 
where m.Win_Type = 1
group by m.Match_Winner 
order by COUNT( m.Match_Id) desc;

--top 5 man of the match player from winning team
select m.Man_of_the_Match,p.Player_Name 
from "Match" m, Player p
inner join "Match" m2 on m.Man_of_the_Match =p.Player_Id 
where m.Match_Winner = 



SELECT * from "Match" m ;






