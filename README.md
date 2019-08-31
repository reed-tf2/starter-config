# Starter Config (For Mastercomfig)

If all you want to do are small things, such as creating an [Uber Bind](https://youtu.be/a8yKrKD1EJg) and/or a [Rocket Jump Script](https://youtu.be/T0nc-jepGVw), this is the config you should use.

## Install

1. Download
   - [Starter Config](https://github.com/rufio-tf2/starter-config/archive/master.zip)
   - [Starter Config (For Mastercomfig)](https://github.com/rufio-tf2/starter-config/archive/for-mastercomfig.zip)
1. Unzip it
1. Navigate into the `starter-config-for-mastercomfig` folder, and move the `user` folder inside into your `tf/cfg` folder
1. Navigate into this `user` folder (`tf/cfg/user`) to add your configurations

## Configure things

### Examples

#### Rocket Jump Script

1. Navigate into the `user` folder installed above: `tf/cfg/user`
1. Open `soldier.cfg`
1. Below the line that says `exec user/allclass`, uncomment the lines (remove the `//` slashes):

   ```
   alias +rocketJump "+jump; +duck; +attack;"
   alias -rocketJump "-jump; -duck; -attack;"
   bind KEY +rocketJump
   ```

1. Change `KEY` to be whatever key you want to use for the rocket jump script
1. Open `allclass.cfg`, and reset the `KEY` to its default command (look [here](https://wiki.teamfortress.com/wiki/List_of_default_keys)). For example, if you used `MOUSE2` (right-click) for the rocket jump script, you should add this:

   ```
   bind MOUSE2 +attack2
   ```

1. Restart TF2

#### Uber Bind

1. Navigate into the `user` folder installed above: `tf/cfg/user`
1. Open `medic.cfg`
1. Below the line that says `exec user/allclass`, uncomment the lines (remove the `//` slashes):

   ```
   alias alertUber "say_team UBER POPPED!!!!!"
   alias +alertAndPopUber "+attack2; alertUber;"
   alias -alertAndPopUber "-attack2;"
   bind MOUSE2 +alertAndPopUber
   ```

1. Open `allclass.cfg`, and reset `MOUSE2` to its default command:

   ```
   bind MOUSE2 +attack2
   ```

1. Restart TF2
