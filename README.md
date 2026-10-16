# Rustler-VR
VR Mod for Rustler

<img width="448" height="442" alt="Adobe" src="https://github.com/user-attachments/assets/e9a790b9-a52c-473c-81b5-149531cf32e4" />

RUSTLER - VR MOD  v0.1.4 (test build Quest 3 VDXR)
==========================================================================
**NEW IN 0.1.12**
* Smoother: "No black outlines" no longer searches every object in the world every few seconds (it looks
  at each person / animal / horse once), and the hand HUD makes far less garbage per frame.
* Still not smooth? Lower "View distance" (VR menu - Picture) - 100 m costs much less than 175-250 m.

**NEW IN 0.1.11**
* Picked-up item texts ("+1 ...") float by your left hand, under the map and objective.
* The wanted level (stars) floats above the health ring and money by your right hand.
* The quest arrows that show where to go now circle the health ring by your right hand (small, still
  pointing the real way) instead of your rustler's feet. VR menu - Hand HUD: "Quest arrows around the
  health ring" and "arrow circle size".

**NEW IN 0.1.9**
* No black outlines (VR menu - Picture - "No black outlines on people / animals", [Camera] NoOutlines):
  switches off the cartoon outline drawn around characters. The log lists what it changed ("Outlines:").

**NEW IN 0.1.8**
* Aim / block moved from LT to RB (the right grip) - with a ranged weapon the laser shows while you aim.
* LT backs your horse up (the game had no gamepad button for it). LB (left grip) + LT = full reverse.
  Both are in [Input] ActionOverrides = Attack2=RB;Mount Backward=LT.

NEW IN 0.1.7
* 6DOF ranged weapons: a bow, crossbow, arquebus or flamethrower sits in the hand holding it (first person,
  or third person with "arms also in third person") and points exactly where that controller points. The
  shot leaves along the weapon - no more shots into the air.
* Laser sight: hold RB (the right grip) with a ranged weapon out. VR menu - Combat - "laser sight":
  Button / Always / Off.
* Live weapon adjust: VR menu - Combat - "Adjust weapon in hand". Hold the OTHER controller's grip to grab
  the weapon and move / turn it in your hand (the laser shows where it shoots), B = back to the default,
  A = save. Saved per weapon type ([Weapon] Offsets).
* Quest objective: its visibility is now read the way the game fades it in, so it should go to your left
  hand. The log notes the quest texts' state ("Hand HUD quest texts").

**NEW IN 0.1.6**
* The right-hand HUD (health ring, money) is whole again - only the left-hand panels have the ring /
  money spots cut out of them.
* The quest objective ("Press ... to show the map" etc.) now goes to your left hand too: every quest text
  (title, objective, timer) gets its own small panel, and its shadow bar leaves the big screen.

**NEW IN 0.1.5**
* Bows, crossbows, guns and throws go where your controller points (also up / down), with no snapping to
  the nearest person. Hold LT or RT and point the hand that holds the weapon: the bow is in his LEFT hand,
  so point with the left controller. VR menu: Combat - "bow / gun aims with" (WeaponHand / Right / Left),
  [Input] AimHand in the config.
* Torch fire (and other effects on his hands) now stays on the torch in first person: the arms are also
  moved to your hands before the game's particles update, not only for the picture.
* Left-hand HUD: the quest box is measured by its text only (its shadow picture made it reach over the
  health ring and money), and any part of the right hand's HUD inside the left panels is cut out
  (and the other way round).

**NEW IN 0.1.4**
* Trees and people no longer dissolve when you get close: the game's "see-through" cone (from its
  top-down camera to your rustler, so he is never hidden) is switched off for its materials in first /
  third person (VR menu: Picture - "No see-through").
* See into the distance: the game only switches on the world about 55 m around its camera. In first /
  third person it now goes out to 250 m (VR menu: Picture - "View distance"; higher = slower).
* Hand HUD: each piece of the HUD gets its own small panel (no big box that takes the health ring and
  money along to the left hand), and they are cut out of the big screen with a wider margin.

**NEW IN 0.1.3**
* Your rustler's arms and hands follow your controllers in first person (the weapon in his hand comes
  along). VR menu: "Arms" (also for third person). Fine-tune: [Arms] HandPosition / HandRotation.
* Trees and people no longer vanish when you get close: the game's occlusion culling (made for the high
  top-down camera) is off for the VR eyes, trees are no longer hidden around you, and the tree tops no
  longer dissolve. VR menu: Picture - "No see-through", "Occlusion culling".
* Left hand: only the quest title / objective with the minimap (the health ring and money no longer
  come along).

**NEW IN 0.1.2**
* Objects no longer vanish when you get close: the game's object optimizers (which hide / simplify things
  its top-down camera can't see) are switched off too (VR menu: "Hiding far / unseen objects" - Off).
* Hand HUD: size, height, forward and outwards for each hand in the VR menu ("Hand HUD"). The pieces
  are centred on that spot (higher by default).
* Right hand: only the health / stamina ring (with your weapon) and the money - the quest text no
  longer comes along. Left hand: minimap and the quest title / objective.

**NEW IN 0.1.1**
* Fixed: blood, tracks and other decals were only drawn in the left eye.
* Swing the right controller to attack with melee weapons - your rustler hits where the controller
  points. The right trigger still attacks too. While LT or RT is held he aims where the right
  controller points (bows, guns, throwing). VR menu: "Combat" (swing on/off, swing speed needed).
* The minimap and the quest objective float by your left controller; health, stamina and money by
  your right controller (VR menu: "Hand HUD" - on/off and size; [UI] ...HandHudOffset for the place).

**INSTALL**
1. Copy the RustlerVR.zip into the game folder (merge / overwrite).
2. Start SteamVR / Quest Link / Virtual Desktop first (it must be the OpenXR runtime), then the game.
   click play when it pops up on steam,when you can hear music in the brown void press Esc
3. Settings: the VR settings menu in the headset (hold Y + left stick click 1.7 s), or
   BepInEx\config\rustler.vr.cfg (made on the first start; changes apply while the game runs).

VIEWS  (hold the RIGHT GRIP and press the RIGHT STICK CLICK to switch)
* Third person (default): you float a few metres behind / above your rustler and look around freely.
  Right stick left / right swings you round him. Distance / height in the VR menu.
  "Third person style" GameCamera = sit where the game's own top-down camera is, looking down on the town.
* First person: you are in your rustler's head, also on horseback (you turn with the horse).
* Cutscenes: you stand where the game's cinematic camera is.
* Left stick "up" walks / rides where you look (VR menu: "Walk / ride direction").
* Menus, dialogs and the HUD are on a floating screen in front of you; use the sticks / d-pad and A / B.

**CONTROLS  (the VR controllers are an Xbox gamepad for the game - its own gamepad layout)**
Right trigger ... RT (swing fire)

Left trigger .... LT (back house up)

Right grip ...... RB (aim\laser)

Left grip ....... LB (sprint player\house)

A ........... (roll)

Y ............... (mount)

X (tap) ......... X

X (hold) ........ Back (map)

X + Y together .. Start (pause)

Left stick click  L3

Right stick up .. d-pad left

Right stick down  d-pad up

Right stick click d-pad down

Right stick left / right  turn (snap 30 degrees)

Right grip + right stick click ... first / third person

Both stick clicks ................ recentre the view

Y + left stick click (hold) ...... VR settings menu

In the game: right grip (RB) = aim / block, left trigger (LT) = horse backs up ([Input] ActionOverrides).

Every button can be changed in [GamepadButtons] of the config file.

NOTES
* horse riding weird
* better to use LG to move single horse foward 

Source code is in BepInEx\plugins\RusVR\source.
