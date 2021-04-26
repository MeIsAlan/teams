Hello there!
Today I'll be showing you a simple way to make teams in the Pawn scripting language.

First we start by making the Player Team Variable
new PlayerTeam[MAX_PLAYERS];

Now we make the teams with Marcos
#define civilians 1
#define admins 2

Now we assign a player to one of the teams, for example when he connects we will assign him to the team of the civilians:
if OnPlayerConnect(playerid)
{
  PlayerTeam[playerid] = civilians;
  SendClientMessage(playerid, 0xFFFFFF, "You have been assigned to a Team!");
}

Now, What if we want to know if that player is an admin?
in some command:
if (PlayerTeam == civilians)
{
  SendClientMessage(playerid, 0xFFFFFF, "You are in the civilians team!");
}
if (PlayerTeam == admins)
{
  SendClientMessage(playerid, 0xFFFFFF, "You are in the Admins Team!");
}

The End! We're done here, Hope this was useful!
