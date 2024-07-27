# Find the City With the Smallest Number of Neighbors at a Threshold Distance

LeetCode Q # 1334.

There are n cities numbered from 0 to n-1. Given the array edges where edges[i] = [fromi, toi, weighti] represents a bidirectional and weighted edge between cities fromi and toi, and given the integer distanceThreshold.

Return the city with the smallest number of cities that are reachable through some path and whose distance is at most distanceThreshold, If there are multiple such cities, return the city with the greatest number.

Notice that the distance of a path connecting cities i and j is equal to the sum of the edges' weights along that path.

Example 1:

<div align = "center">

  ![image](https://github.com/user-attachments/assets/4a2a5a7c-d7e4-4081-ab55-4cdfaa47a899)

</div>

> Input: n = 4, edges = [[0,1,3],[1,2,1],[1,3,4],[2,3,1]], distanceThreshold = 4</br>
> Output: 3</br>
> Explanation: The figure above describes the graph. </br>
> The neighboring cities at a distanceThreshold = 4 for each city are:</br>
> City 0 -> [City 1, City 2] </br>
> City 1 -> [City 0, City 2, City 3] </br>
> City 2 -> [City 0, City 1, City 3] </br>
> City 3 -> [City 1, City 2] </br>
> Cities 0 and 3 have 2 neighboring cities at a distanceThreshold = 4, but we have to return city 3 since it has the greatest number.

Example 2:

<div align = "center">

  ![image](https://github.com/user-attachments/assets/295f9153-576a-41f6-adc6-ab57f84da676)

</div>

> Input: n = 5, edges = [[0,1,2],[0,4,8],[1,2,3],[1,4,2],[2,3,1],[3,4,1]], distanceThreshold = 2</br>
> Output: 0</br>
> Explanation: The figure above describes the graph. </br>
> The neighboring cities at a distanceThreshold = 2 for each city are:</br>
> City 0 -> [City 1] </br>
> City 1 -> [City 0, City 4] </br>
> City 2 -> [City 3, City 4] </br>
> City 3 -> [City 2, City 4]</br>
> City 4 -> [City 1, City 2, City 3] </br>
> The city 0 has 1 neighboring city at a distanceThreshold = 2.

My Solution Analysis:

<div align = "center">

  ![image](https://github.com/user-attachments/assets/c550f027-2c61-4dc3-a85b-14ef956490fc)

  Time complexity: O(n^3).</br>Space complexity: O(n^2).
</div>
