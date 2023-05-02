Download Link: https://assignmentchef.com/product/solved-cop3330-object-oriented-programming-euchre-project-part-6
<br>
<strong>Assignment Scope        </strong>

<strong> </strong>

For this assignment each player will either accept or reject the trump suit.  If the player accepts the trump suit they say “Pick it up!”  If the player rejects the trump suit they say “Pass.”  The human player will be able to respond as desired.  For the AI players it will depend upon how many cards in their hand match the trump suit.  For our purposes we will implement the version of Euchre called “Stick the Dealer.”  What that means is, if every player passes on the trump suit the dealer has to accept it!




To accomplish this:

<ol>

 <li>Reference the tasks below for the specifics of the source code requirements.</li>

 <li>Compress a project and submit to Webcourses</li>

 <li>Decompress compressed project and verify it is a Netbeans project</li>

</ol>




<strong>References</strong>

<ol>

 <li>docx</li>

 <li>Setting up a project in Netbeans.docx</li>

 <li>Netbeans right click menu help.docx</li>

</ol>




<strong>Deliverables</strong>

To complete this assignment, you must submit your <strong>compressed Netbeans project </strong>to Webcourses.




Please keep in mind that the tasks are guidance to accomplish the goals of the assignment.  At times students will be required to do additional research (e.g. Google That S**T (GTS)!) to find implementation options.  In the industry, software engineers are <strong><u>expected</u></strong> to be very self-sufficient to find the best solution for the task at hand.




<strong><em>I have provided multiple code examples on Webcourses that shows how to implement numerous of the tasks below, please reference those code examples prior to asking me for help!    </em></strong>

<strong> </strong>

<strong>Tasks and Rubric</strong>

<table width="682">

 <tbody>

  <tr>

   <td colspan="3" width="682"><strong>Activity</strong></td>

  </tr>

  <tr>

   <td width="180"><strong>euchre package</strong></td>

   <td width="502"> </td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>constants package</strong></td>

   <td width="502"> </td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>Constants.java</strong></td>

   <td width="502">1.      Update class to add the following constanta.       MAX_PASSES = 3b.      MIN_TRUMP = 3</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>core package</strong></td>

   <td width="502"> </td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>AiPlayer.java</strong></td>

   <td width="502">1.      Update class to add the following member variablesa.       Game game2.      Add a setter for member variable of class Game3.      Update method makeTrump() so it does the followinga.       Checks if the max number of passes has been reached (i.e. 3) by calling method getTrumpCheck from class Gamei.      If true, display a message dialog to the player (i.e. the dealer) that they have to accept trumpii.      Call method setAcceptTrump passing as an argument the value trueb.      Elsei.      Create a local variable to count how many cards the player has of the trump suitii.      Loop through the player’s hand, for each card in their hand1.      Check if the current card’s suit matches the trump card’s suit2.      HINT: reference member variable of class Game calling method getTrump to retrieve the trump cardiii.      Check if the trump counter is greater than or equal the value of 3 (e.g. this is a good indicator the team will win the hand)1.      If true, call method setAcceptTrump() passing as an argument the value true2.      Display a message dialog stating that the current player has said “Pick it Up!”iv.      Else1.      Call method setAcceptTrump() passing as an argument the value false2.      Display a message dialog stating that the current player has said “Pass!”</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>Game.java</strong></td>

   <td width="502">1.      Update class to add the following member variablesa.       int trumpCheckb.      Team trumpTeam</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong> </strong></td>

   <td width="502">2.      Add a getter for member variable trumpCheck3.      Update customer constructor Game() to do the followinga.       Comment out the call the method play()4.      Update method createTeams() to do the followinga.       On the instance of class HumanPlayer, call method setGame() passing as an argument a reference to this class Gameb.      On the instance of class AiPlayer, call method setGame() passing as an argument a reference to this class Game5.       Update method play() to do the followinga.       Comment out any current codeb.      Add a call to method trumpCheck6.      Add method trumpCheck to do the followinga.       Return type voidb.      Empty parameter listc.       Initialize member variable trumpCheck to the value of 0d.      Create a local variable of data type int to represent the current player, initialized to the member variable leadIdxe.       Loop while the value of member variable trumpCheck is less than the number of playersi.      Instantiate an instance of class Player set equal to member variable getting the player at the position represented by local variable created in step d. (i.e. starting with the lead player)ii.      On the Player object from above, call method makeTrump()iii.      Check if the Player object accepted the trump by calling method getAcceptTrump()1.      If true, loop through the member variable of data type ArrayList that stores the teams in the game2.      Check if the current team contains the current player (HINT: use method contains() that is part of the class ArrayList)a.       If true, set the member variable trumpTeam equal to the current teamb.      Display a dialog message to state which team has accepted the trump suit3.      Break out of the while loop if trump has been acceptediv.      Else1.      Increment the member variable trumpCheck by onev.      Increment the local variable representing the current player by one; be sure to check if the counter is equal to 3, then reset it to 0 (e.g. remember, the table member variable has only 4 elements so the maximum index is 3)</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>HumanPlayer.java</strong></td>

   <td width="502">1.      Update class to add the following member variablesa.       Game game2.      Add a setter for member variable of class Game3.      Update method makeTrump() so it does the followinga.       Checks if the max number of passes has been reached (i.e. 3) by calling method getTrumpCheck from class Gamei.      If true, display a message dialog to the player (i.e. the dealer) that they have to accept trumpii.      Call method setAcceptTrump passing as an argument the value trueb.      Elsei.      Create a local variable set equal to JOptionPane.showConfirmDialog static method call prompting the human player if they accept the trump suitii.      If the human player’s response is true,1.      Call method setAcceptTrump() passing as an argument the value trueiii.      Else1.      Call method setAcceptTrump() passing as an argument the value false</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>Player.java</strong></td>

   <td width="502">1.      Update class to add the following member variablea.       boolean acceptTrump2.      Generate a getter/setter for the member variable acceptTrump</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>images package</strong></td>

   <td width="502"> </td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>userInterface package</strong></td>

   <td width="502"> </td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>AiPlayerUi.java</strong></td>

   <td width="502">1.      Update the class to add the following member variablesa.       GameUi gameUi2.      Modify the custom constructor to do the followinga.       Add a third parameter of data type class GameUib.      On the member variable of class AiPlayer, call method setUi passing as an argument the parameter of class GameUi</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>GameUi.java</strong></td>

   <td width="502">1.      Update the class to add the following member variablesa.       JPanel trumpPanel (if you added bidPanel in the last assignment, please rename it)b.      JLabel teamOneScoreLblc.       JLabel teamOneScored.      JLabel teamTwoScoreLble.       JLabel teamTwoScoref.        JLabel trumpCard</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong> </strong></td>

   <td width="502">2.      Update initComponents to do the followinga.       Trump Panel1.      Instantiate the JPanel member variable for the trump panel2.      Instantiate the JLabel member variable for the trump label3.      Instantiate an instance of class CardUi passing as arguments to the constructor the followingi.            JLabel member variable for the trump cardii.            The trump card’s face valueiii.            The trump card’s suitiv.            Update the JLabel member variable for the trump to do the followinga.       setting it equal to method call getLabel on the instance of class CardUib.      add client property passing arguments “face” and the trump card’s face valuec.       add client property passing arguments “suit” and the trump card’s suitv.            Add the trump card JLabel the the trump panel4.      Add the trump JPanel to the north JPanelb.      Score Panel1.      Use layout manager GridLayout so it is a 2 x 2 grid2.      Instantiate the following member variables of class JLabeli.            teamOneScoreLbl with text “Team One”ii.            teamOneScore with text using the following method call: game.getTeams().get(Constants.ONE).getTeamScore()iii.            teamOneScoreLbl with text “Team Two”iv.            teamOneScore with text using the following method call: game.getTeams().get(Constants.TWO).getTeamScore()3.      Add the four JLabels to the score JPanel4.      Add the score JPanel the the north JPanelc.       For the four player JPanels, aiOnePanel, aiTwoPanel, aiThreePanel, and hpPanel1.      Add an additional argument to the constructor calls a reference to this class, GameUi</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>HumanPlayerUi.java</strong></td>

   <td width="502">1.      Update the class to add the following member variablesa.       GameUi gameUi2.      Modify the custom constructor to do the followinga.       Add a second parameter of data type class GameUi1.      On the member variable of class HumanPlayer, call method setUi passing as an argument the parameter of class GameUi</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>Euchre application</strong></td>

   <td width="502"> </td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>Test Cases </strong></td>

   <td width="502">Test Cases pass</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong> </strong></td>

   <td width="502">Source compiles with no errors</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong> </strong></td>

   <td width="502">Source runs with no errors</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong> </strong></td>

   <td width="502">Source includes comments</td>

   <td width="0"> </td>

  </tr>

  <tr>

   <td width="180"><strong>Total</strong></td>

   <td width="502"><strong> </strong></td>

   <td width="0"> </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong>Perform the following test cases</strong>

<table width="638">

 <tbody>

  <tr>

   <td colspan="3" width="638"><strong>Test Cases</strong></td>

  </tr>

  <tr>

   <td width="97"><strong> </strong></td>

   <td width="250"><strong>Action</strong></td>

   <td width="291"><strong>Expected outcome</strong></td>

  </tr>

  <tr>

   <td width="97"><strong>Test Case 1</strong></td>

   <td width="250"><strong>Regression Testing: Initial JOptionPane displays </strong></td>

   <td width="291">JOptionPane is similar to figure 1</td>

  </tr>

  <tr>

   <td width="97"><strong>Text Case 2</strong></td>

   <td width="250"><strong>Regression Testing: JOptionPane Prompts User Name</strong></td>

   <td width="291">JOptionPane is similar to figure 2</td>

  </tr>

  <tr>

   <td width="97"><strong>Test Case 3</strong></td>

   <td width="250"><strong>Euchre Initial UI displays</strong></td>

   <td width="291">Game UI looks similar figure 3 where:1.      The score panel displays2.      The trump panel displays</td>

  </tr>

  <tr>

   <td width="97"><strong>Test Case 4</strong></td>

   <td width="250"><strong>Regression Testing: Project view</strong></td>

   <td width="291">Project view matches figure 4</td>

  </tr>

  <tr>

   <td width="97"><strong>Test Cases 5, 6, 7, 8</strong></td>

   <td width="250"><strong>The result of each player accepting or rejecting the trump suit should display</strong></td>

   <td width="291">Game UI looks similar to figures 5, 6, 7, and 8</td>

  </tr>

  <tr>

   <td width="97"><strong>Test Case 9</strong></td>

   <td width="250"><strong>The team that called trump</strong></td>

   <td width="291">UI looks similar to figure 9</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong> </strong>

Figure 1 Intro JOptionPane

<strong> </strong>




Figure 2 Prompt for User’s Name




Figure 3 Euchre Initial UI













Figure 4 Project View

Figure 5 Lead Player




Figure 6 Next Player




Figure 7 Next Player




Figure 8 Dealer







Figure 9 Trump Team


