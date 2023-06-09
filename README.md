# Algorithm which visualize permutations simulation
## Demo
![15](https://user-images.githubusercontent.com/123249470/231189581-51d0d722-ac05-4046-ba7f-db6fef748286.gif)
![15](https://user-images.githubusercontent.com/123249470/231208904-8a680d4d-275e-4217-9d9d-5b35cd1ee8fa.gif)
## Customize it by yourself

### Change the position and the amount of circles
  Set the number of the objects by changing index value (```n``` is default):
```c++
Object circle[n];
```
Set position of the objects based on index value (to ```n-1```):
```c++
circle[0].set_pos(500, 100);
circle[1].set_pos(800, 50);
circle[2].set_pos(200, 700); 
.
.
.
circle[n-1].set_pos(400, 300); 
 ```
Change the value of an array that holds the maximum value of the permutation:
 ```c++
int a[] = { 0, 1, 2, ... , n-1};
 ```
### Example of changed code
 ```c++
Object circle[4];

circle[0].set_pos(500, 100);
circle[1].set_pos(800, 50);
circle[2].set_pos(200, 700);
circle[3].set_pos(150, 300);

int a[] = { 0, 1, 2, 3};
 ```
 ### Change colors:
 in class ```Object```
  ```c++
  class Object
{
public:
.
.
.
  void render(sf::RenderWindow& window, bool hasLineConnection) {
      circle.setPosition(pos);
      circle.setRadius(20);
      if (hasLineConnection) {
          circle.setFillColor(sf::Color::Cyan); //Change color of active circles(connected to line)
      }
      else {
          circle.setFillColor(sf::Color::White); //Change color of none active circles
      }
 ```
Note: algorithm visualization is based on SFML c++ library
## How to Contribute
1. Fork the Project
2. Clone repo with your GitHub username instead of ```YOUR-USERNAME```:<br>
```
$ git clone https://github.com/YOUR-USERNAME/Permutation_Simulation
```
3. Create new branch:<br>
```
$ git branch BRANCH-NAME 
$ git checkout BRANCH-NAME
```
4. Make changes and test<br>
5. Submit Pull Request with comprehensive description of change
## Task list
* <del> upgrade graphics<br> </del>
* <del> split into files and organize code<br></del>
* <del> function that finds range between objects<br></del>
* <del> function that return progress in percentage<br></del>

## What I have learned
•	improved SFML library skills<br>
•	the basics of algorithmics

## License 
[MIT license](LICENSE.md)

