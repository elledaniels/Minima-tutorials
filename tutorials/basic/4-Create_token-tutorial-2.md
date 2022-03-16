------------------------------------------------------------
### **Tutorial 4**: Learning how to create Tokens part 2, before, **you will need 2 minimas**
#### The important part of this tutorial is to open your mind to realise how powerful tokens can be and diffent ways to use and apply on several use cases.

#### Another important part of this tutorial is to realise that when you execute **balance** command, what terminal prompts is the sum of all your minimas that you have on the several addresses of your node and a list of tokens that your node has with some properties prompt, to see that a **balance** shows the sum of all your minimas we are going to use the commmand **coins relevant:true** that will show you every wallet address of your node that has minimas or tokens and their quantity on every address and this is important part when you use the **splitter** function of the app-game provided.
-----------------------------------------------------------
-1: **Download** the app-game:
  - Linux version: <https://mega.nz/file/svZGGRIL#e2qixE5EEZa_wSqqqOcnFuwpXiYM4SlGY9oNW5tJttY>
  - Windows version: <https://mega.nz/file/pu4DVYrD#OrgdxLsvzjrHpq7VDAmiMstp38z6sHu1D7pe0veqn2s>
  - Android version (not playable): <https://mega.nz/file/h6xgRaIb#KONVzl7Q05zpuVBS1fFqji7YyZ2bnfQwIRlOxpDYn50>
  The android version is not playable as it doesn't have pads to move the player and it is only to show that if your node receive a power token, the player will change accordingly to what the token properties are.
- Note: If you download the mobile version, you first need to run this command on the minima terminal, otherwise the app-game it won't work, execute command: ` rpc enable:true ` this command it lets your node to receive commands at port 9002, so if you know your wifi IP you could send the commands via webpage also.

-2: **Execute** the app-game and click **New Game** but don't play the game yet, just watch the color and the size of the player, becouse if you only have the two minimas required then you can have problems following the tutorial on the next steps, now quit the game but not from the app.
  - Option 1: create the power token using the terminal provided in the app, if you are on a mobile this terminal it will let you copy values as in the minima terminal it dosen't work.
  - Option 2: create the power token using the usual way you send commands to your minima node.

-3: **Create the power token** executing the following command: ` tokencreate name:{"name":"POWER_1","color":"#FF0000","size":2} amount:1 decimals:0 `
  - We are only interested in 1(amount) token and 0 (decimals)
  - If you look at the help about "tokencreate" it finished with "name can be a JSON Object"
  - What is a JSON Object ?
    - A JSON Object is a structure that let you define "things" with a set of properties and values separated them by ` : `
    - A JSON Object must start and end with ` {} `
    - Every property defined must have a value and the every ` property:value ` group must be separated by ` , `
    - So, in our example we have **three properties** defined on the Token we created.
      - The **name** the requirement in the game is that it needs to begin with "POWER_" and whatever you wants, the game only checks for that requirement.
      - The **color** it must be a valid RGB color and will be the player color, the one provided is RED color, here there is a link where you can find RGB color values to experiment: <https://www.rapidtables.com/web/color/RGB_Color.html>
      - The **size** is the size/scale of the player and the values should be between 0.2 and less than 3, values under 1 makes the player smaller and values over 1 makes the player bigger.The values are not checked so if you introduce other values will produce unexpected results that could be solved simply sending away the token you created to another node or create a new token (Theoretically the new token received/created should be taken than the older, but is not checked, it is the order on how "balance" command prompts the results )
    - There is no socket listener for events on the actual minima version as it was deleted from the previous one, so the balance is checked every 30 seconds, so when you receive/create a token, you will have to wait a time for the transaction to be publish thru the network and the changes to be reflected on the player will not be instant due to those explained reasons.
    - **Once the token is created** just go to the game, without playing yet, and observe how the player change when the token is received, you could check your "balance" and you will see the token received and remember that it can take a few minutes to receive/create the token and be publish to the network.
    - Executing command: ` balance ` to show the info of the token created, you should see something like that:
```
  {
    "token":{
      "name":"POWER_1",
      "color":"#FF0000",
      "size":2
    },
    "tokenid":"0xC18122B724055D1BF76CBDD6F862F1E2FACD13C02F39A9ABE5D5A330987AF594",
    "confirmed":"0",
    "unconfirmed":"1",
    "sendable":"0",
    "total":1
  },
```
-4: ----under construction.....
