Hi! this is a documentary of the menu template I made for Gorilla Tag (vr game) Copies (fan games using the original assets)
This is also included in the unity package if you want to look over it.
(WARNING! This is a slighty edited version.)

While the menu script doesn't have a full-fledged API, it does have some variables that can be changed with c#:

Dependencies/Setup
Create a new c# script in Extensions or whatever location you want.
Add "public ModMenu MenuScript" to it.
You're ready to go!

# BASICS:

## color
this one is built into v1.1, called "ThemeChanger"
## DEPENDENCIES
MenuScript

(replace [colorvar] with a Color variable you have created.)
________________________________________________________________________________________________________________________________
	MenuScript.BGColor = [colorvar];
	MenuScript.ButtonColor = [colorvar];
	MenuScript.PressedColor = [colorvar];
________________________________________________________________________________________________________________________________
## single tap support
This one is easier to understand with code
________________________________________________________________________________________________________________________________
	private void OnEnable()
	{
		gameObject.SetActive(false);
	}
________________________________________________________________________________________________________________________________
## Redirect
When you press a button, it goes to a different category
## DEPENDENCIES

single tap support

MenuScript
________________________________________________________________________________________________________________________________
	public int Category;
	public bool left; // <<< optional

	MenuScript.Home();
	MenuScript.TurnPage(left); // <<< optional
	MenuScript.EnterCategory(Category);
________________________________________________________________________________________________________________________________ 
Thats all for V1.1, this may be updated in the future.
