# admin-panel-v1-
╔══════════════════════════════════════════════════════════════════════════════╗
║              🚀 QUICK INSTALLATION GUIDE - 3 SIMPLE STEPS                    ║
╚══════════════════════════════════════════════════════════════════════════════╝

┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ STEP 1: PLACE THE FILES                                                    ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

Open Roblox Studio → Your Game → Explorer Window

1️⃣ Put AdminSystem_Server.lua in:
   ServerScriptService
   
   How:
   • Right-click ServerScriptService
   • Insert Object → Script
   • Delete the default code
   • Paste AdminSystem_Server.lua content
   • Name it: "AdminSystem_Server"


2️⃣ Put AdminSystem_Client.lua in:
   StarterPlayer → StarterPlayerScripts
   
   How:
   • Expand StarterPlayer in Explorer
   • Right-click StarterPlayerScripts
   • Insert Object → LocalScript
   • Delete the default code
   • Paste AdminSystem_Client.lua content
   • Name it: "AdminSystem_Client"


3️⃣ Put TitleSystem_Client.lua in:
   StarterPlayer → StarterPlayerScripts
   
   How:
   • Right-click StarterPlayerScripts again
   • Insert Object → LocalScript
   • Delete the default code
   • Paste TitleSystem_Client.lua content
   • Name it: "TitleSystem_Client"


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ STEP 2: ADD YOUR USERID                                                    ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

🔍 How to find your UserId:

Method 1 (Website):
  • Go to: roblox.com/users/YOUR_PROFILE
  • Look at the URL
  • Example: roblox.com/users/123456789/profile
  • Your UserId = 123456789

Method 2 (Studio):
  • In Roblox Studio, press Play
  • Open Output window
  • Paste this in Command Bar:
    print(game.Players.LocalPlayer.UserId)
  • Press Enter
  • Your UserId will appear in Output


✏️ Edit AdminSystem_Server.lua:

Find this section (around line 30):

    RankList = {
        [1] = "Owner",        -- ← Replace 1 with YOUR UserId
        [2] = "Admin",
        [3] = "Mod",
        [4] = "Support",
    },

Change it to:

    RankList = {
        [123456789] = "Owner",    -- ← Your real UserId here!
        -- Add friends below:
        -- [987654321] = "Admin",
        -- [111222333] = "Mod",
    },


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ STEP 3: TEST THE SYSTEM                                                    ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

1. Click "Play" in Roblox Studio (F5)

2. Check Output window for:
   "ADMIN PANEL SYSTEM - INITIALIZED" ✓

3. Press the ";" key (semicolon) on your keyboard
   → Admin panel should open with RGB border!

4. Try a command in chat:
   ;heal me
   
5. Try the title system:
   ;title me OWNER
   ;rgbtitle me


🎉 SUCCESS! You now have a fully working admin system!


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ 📱 KEYBOARD SHORTCUTS                                                      ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

; (Semicolon)     Toggle Admin Panel
Click & Drag      Move the panel anywhere
Esc              Close panel (click X button)


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ ⚡ QUICK COMMAND EXAMPLES                                                  ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

Type in chat (must start with ; ):

;heal PlayerName              Heal a player
;speed PlayerName 100         Make them super fast
;title PlayerName VIP         Give them a VIP title
;rgbtitle PlayerName          RGB animated title
;titlecolor PlayerName 255 0 0   Red title
;freeze PlayerName            Freeze them in place
;tp PlayerName                Teleport to them
;kick PlayerName Being rude   Kick with reason
;global Server restart soon!  Announce to everyone


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ ❗ COMMON MISTAKES                                                         ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

❌ Forgetting the ";" prefix
   Wrong: heal me
   Right: ;heal me

❌ Using Script instead of LocalScript for client files
   • AdminSystem_Client.lua = LocalScript
   • TitleSystem_Client.lua = LocalScript
   • AdminSystem_Server.lua = Script (not LocalScript)

❌ Not editing the UserId
   • Must replace [1] with your real UserId
   • Don't leave it as [1] or [2]

❌ Putting files in wrong locations
   • Server script goes in ServerScriptService
   • Client scripts go in StarterPlayerScripts


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ 🎨 CUSTOMIZATION TIPS                                                      ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

Want to change colors?
→ Edit AdminSystem_Client.lua, look for "UIConfig" section

Want different commands?
→ Edit AdminSystem_Server.lua, find "Commands" table

Want to change the toggle key?
→ Edit AdminSystem_Client.lua, find "ToggleKey"

Want to add more ranks?
→ Edit AdminSystem_Server.lua, modify "Ranks" table


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ 🛡️ SECURITY REMINDER                                                      ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

✓ This system is EXPLOIT-PROOF
✓ All commands validated server-side
✓ Players cannot fake permissions
✓ Only people in RankList can use commands
✓ Bans are saved permanently


═══════════════════════════════════════════════════════════════════════════════

                        ✅ INSTALLATION COMPLETE!
                    Press ; to open your admin panel
                         See README.txt for more

═══════════════════════════════════════════════════════════════════════════════
╔══════════════════════════════════════════════════════════════════════════════╗
║                    🎮 PROFESSIONAL ADMIN PANEL SYSTEM                        ║
║                          Production-Ready v1.0                               ║
╚══════════════════════════════════════════════════════════════════════════════╝

📋 TABLE OF CONTENTS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. Installation Structure
2. File Descriptions
3. Configuration Guide
4. Command List
5. Features Overview
6. Security Notes
7. Troubleshooting


═══════════════════════════════════════════════════════════════════════════════
1. 📁 INSTALLATION STRUCTURE
═══════════════════════════════════════════════════════════════════════════════

Place files in the following locations in Roblox Studio:

📦 Your Roblox Game
 ┣ 📂 ServerScriptService
 ┃ ┗ 📜 AdminSystem_Server.lua
 ┃
 ┣ 📂 StarterPlayer
 ┃ ┗ 📂 StarterPlayerScripts
 ┃   ┣ 📜 AdminSystem_Client.lua
 ┃   ┗ 📜 TitleSystem_Client.lua
 ┃
 ┗ 📂 ReplicatedStorage
   ┗ 📁 AdminRemotes (created automatically by server script)


═══════════════════════════════════════════════════════════════════════════════
2. 📄 FILE DESCRIPTIONS
═══════════════════════════════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────────────────────────────┐
│ 📜 AdminSystem_Server.lua                                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│ Location: ServerScriptService                                              │
│ Type: Server Script                                                         │
│ Purpose: Core admin system - handles all commands, permissions, bans,      │
│          security, and server-side logic                                    │
│                                                                             │
│ Key Features:                                                               │
│ • Rank-based permission system                                             │
│ • Chat command parsing                                                      │
│ • Ban/kick/warn system with DataStore                                      │
│ • Title system management                                                   │
│ • Action logging                                                            │
│ • Anti-spam protection                                                      │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│ 📜 AdminSystem_Client.lua                                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│ Location: StarterPlayer > StarterPlayerScripts                             │
│ Type: Local Script                                                          │
│ Purpose: Creates and manages the admin panel UI                            │
│                                                                             │
│ Key Features:                                                               │
│ • RGB animated neon UI                                                      │
│ • Draggable window                                                          │
│ • Player list with search                                                   │
│ • Action panel with quick commands                                          │
│ • Notification system                                                       │
│ • Mobile support                                                            │
│ • Toggle with ";" key                                                       │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│ 📜 TitleSystem_Client.lua                                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│ Location: StarterPlayer > StarterPlayerScripts                             │
│ Type: Local Script                                                          │
│ Purpose: Handles player title rendering and RGB animations                 │
│                                                                             │
│ Key Features:                                                               │
│ • Billboard GUI above player heads                                          │
│ • RGB gradient animation                                                    │
│ • Custom colors and text                                                    │
│ • Auto-respawn handling                                                     │
│ • Smooth entrance/exit animations                                           │
│ • Glow effects                                                              │
└─────────────────────────────────────────────────────────────────────────────┘


═══════════════════════════════════════════════════════════════════════════════
3. ⚙️ CONFIGURATION GUIDE
═══════════════════════════════════════════════════════════════════════════════

🔧 STEP 1: Edit AdminSystem_Server.lua
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Find this section (around line 30):

    RankList = {
        -- Example UserIds (replace with real ones)
        [1] = "Owner",        -- Replace with your UserId
        [2] = "Admin",
        [3] = "Mod",
        [4] = "Support",
        -- Add more users here
    },

📝 How to get your UserId:
   1. Go to roblox.com/users/YOUR_PROFILE
   2. Look at the URL - the number is your UserId
   3. Or use this in Studio: print(game.Players.LocalPlayer.UserId)

✏️ Example Configuration:

    RankList = {
        [123456789] = "Owner",      -- Your UserId
        [987654321] = "Admin",      -- Friend's UserId
        [555555555] = "Admin",      -- Another admin
        [111111111] = "Mod",        -- Moderator
        [222222222] = "Support",    -- Support staff
    },


🔧 STEP 2: Customize Settings (Optional)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

You can change these settings in AdminSystem_Server.lua:

    Prefix = ";",              -- Command prefix (default: ;)
    MinRankForPanel = 3,       -- Minimum rank to see panel (3 = Mod)
    CommandCooldown = 1,       -- Seconds between commands


🔧 STEP 3: Test the System
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. Start a test server in Roblox Studio
2. Check Output for: "ADMIN PANEL SYSTEM - INITIALIZED"
3. Press ";" key to open the admin panel
4. Try a command: ;heal me


═══════════════════════════════════════════════════════════════════════════════
4. 💬 COMMAND LIST
═══════════════════════════════════════════════════════════════════════════════

All commands start with ";" (semicolon)

┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ 🛡️ MODERATION COMMANDS                                                     ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

;kick <player> [reason]
  ├─ Permission: Mod (3+)
  ├─ Example: ;kick john Spam
  └─ Description: Kicks player from server

;ban <player> [reason]
  ├─ Permission: Admin (4+)
  ├─ Example: ;ban john Exploiting
  └─ Description: Permanently bans player

;tempban <player> <time> [reason]
  ├─ Permission: Admin (4+)
  ├─ Example: ;tempban john 5m Rude behavior
  ├─ Time formats: 5s, 10m, 2h, 1d
  └─ Description: Temporarily bans player

;unban <userId>
  ├─ Permission: Admin (4+)
  ├─ Example: ;unban 123456789
  └─ Description: Unbans a player by UserId

;warn <player> [reason]
  ├─ Permission: Support (2+)
  ├─ Example: ;warn john Stop jumping
  └─ Description: Sends warning to player


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ 👤 PLAYER CONTROL COMMANDS                                                 ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

;freeze <player>
  ├─ Permission: Mod (3+)
  ├─ Example: ;freeze john
  └─ Description: Freezes player in place

;unfreeze <player>
  ├─ Permission: Mod (3+)
  ├─ Example: ;unfreeze john
  └─ Description: Unfreezes player

;speed <player> <number>
  ├─ Permission: Admin (4+)
  ├─ Example: ;speed john 50
  └─ Description: Sets player walk speed

;jump <player> <number>
  ├─ Permission: Admin (4+)
  ├─ Example: ;jump john 100
  └─ Description: Sets player jump power

;heal <player>
  ├─ Permission: Mod (3+)
  ├─ Example: ;heal john
  └─ Description: Heals player to full health

;kill <player>
  ├─ Permission: Admin (4+)
  ├─ Example: ;kill john
  └─ Description: Kills the player


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ 🌟 TELEPORT COMMANDS                                                       ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

;tp <player>
;goto <player>
  ├─ Permission: Mod (3+)
  ├─ Example: ;tp john
  └─ Description: Teleports you to player

;bring <player>
  ├─ Permission: Admin (4+)
  ├─ Example: ;bring john
  └─ Description: Brings player to you


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ 🏷️ TITLE COMMANDS (NEW!)                                                   ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

;title <player> <text>
  ├─ Permission: Admin (4+)
  ├─ Example: ;title john VIP PLAYER
  └─ Description: Gives player a custom title

;titlecolor <player> <R> <G> <B>
  ├─ Permission: Admin (4+)
  ├─ Example: ;titlecolor john 255 100 200
  └─ Description: Changes title color (RGB values 0-255)

;rgbtitle <player>
  ├─ Permission: Admin (4+)
  ├─ Example: ;rgbtitle john
  └─ Description: Enables RGB rainbow animation on title

;removetitle <player>
  ├─ Permission: Admin (4+)
  ├─ Example: ;removetitle john
  └─ Description: Removes player's title


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ 🎉 FUN & EVENT COMMANDS                                                    ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

;fire <player>
  ├─ Permission: Admin (4+)
  ├─ Example: ;fire john
  └─ Description: Sets player on fire

;sparkles <player>
  ├─ Permission: Admin (4+)
  ├─ Example: ;sparkles john
  └─ Description: Adds sparkles to player


┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ 🌐 SERVER COMMANDS                                                         ┃
┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛

;global <message>
;servermsg <message>
  ├─ Permission: Admin (4+)
  ├─ Example: ;global Server restart in 5 minutes!
  └─ Description: Sends announcement to all players

;shutdown [reason]
  ├─ Permission: Owner (5)
  ├─ Example: ;shutdown Maintenance
  └─ Description: Shuts down the server


═══════════════════════════════════════════════════════════════════════════════
5. ✨ FEATURES OVERVIEW
═══════════════════════════════════════════════════════════════════════════════

🎨 USER INTERFACE
  ✓ RGB animated neon borders
  ✓ Dark transparent glass-morphism design
  ✓ Smooth animations (open/close/hover)
  ✓ Fully draggable window
  ✓ Player search functionality
  ✓ Mobile-responsive design
  ✓ Quick action buttons
  ✓ Real-time player list

👑 RANK SYSTEM
  ✓ 5 permission levels: Owner, Admin, Mod, Support, User
  ✓ UserId-based assignment
  ✓ Permission-based command access
  ✓ Automatic rank badges in UI

🏷️ TITLE SYSTEM
  ✓ Custom text above player heads
  ✓ RGB animated gradient titles
  ✓ Custom color support (RGB values)
  ✓ Persists through respawns
  ✓ Visible to all players
  ✓ Smooth animations
  ✓ Glow effects

🔒 SECURITY
  ✓ All validation server-side only
  ✓ Client cannot bypass permissions
  ✓ Protected RemoteEvents
  ✓ Ban data stored in DataStore
  ✓ Anti-spam cooldown system
  ✓ Command logging

📢 NOTIFICATIONS
  ✓ On-screen notifications
  ✓ Color-coded by severity
  ✓ Auto-dismiss after 5 seconds
  ✓ Smooth slide-in animations
  ✓ Shows admin name on actions

💾 DATA PERSISTENCE
  ✓ Permanent bans saved to DataStore
  ✓ Temporary bans with expiration
  ✓ Auto-load on server start


═══════════════════════════════════════════════════════════════════════════════
6. 🔐 SECURITY NOTES
═══════════════════════════════════════════════════════════════════════════════

⚠️ IMPORTANT SECURITY FEATURES:

✓ Server-Side Validation
  • All commands processed on server
  • Client cannot fake permissions
  • No client-side exploits possible

✓ Permission Checks
  • Every command checks rank
  • Players can't use higher-rank commands
  • Automatic permission denial

✓ Input Sanitization
  • Player names validated
  • Command arguments checked
  • Prevents injection attacks

✓ Remote Protection
  • RemoteEvents check caller permission
  • No direct client manipulation
  • Secure command parsing

✓ Ban System
  • Bans stored in DataStore
  • Checked on player join
  • Automatic kick if banned


⚡ ANTI-EXPLOIT MEASURES:

  1. Commands only work from verified admins
  2. All actions logged with admin name
  3. Cooldown prevents command spam
  4. UI buttons trigger server validation
  5. No client-side trust


═══════════════════════════════════════════════════════════════════════════════
7. 🔧 TROUBLESHOOTING
═══════════════════════════════════════════════════════════════════════════════

❌ Problem: Admin panel won't open
   ✓ Solution: 
     • Check if your UserId is in RankList
     • Verify rank is 3 or higher (Support+)
     • Press ";" key (semicolon)
     • Check Output for errors

❌ Problem: Commands don't work
   ✓ Solution:
     • Make sure to use ";" prefix
     • Check your permission level
     • Use correct spelling: ;kick not ;kik
     • Try in chat, not panel initially

❌ Problem: Titles don't appear
   ✓ Solution:
     • Verify TitleSystem_Client.lua is in StarterPlayerScripts
     • Wait 1-2 seconds after giving title
     • Respawn to refresh
     • Check Output for errors

❌ Problem: RGB effects not working
   ✓ Solution:
     • This is normal - they animate in real-time
     • May appear as static color in screenshots
     • Test in-game, not in Studio edit mode

❌ Problem: Player list is empty
   ✓ Solution:
     • Click "Refresh" or reopen panel
     • Make sure other players are in game
     • Check server script is running

❌ Problem: Bans don't save
   ✓ Solution:
     • Enable Studio Access to API Services
     • Game Settings → Security → Enable Studio Access
     • Publish game to Roblox
     • DataStores only work in published games


═══════════════════════════════════════════════════════════════════════════════
8. 📞 SUPPORT & CUSTOMIZATION
═══════════════════════════════════════════════════════════════════════════════

🎨 CUSTOMIZATION IDEAS:

  • Change UI colors in AdminSystem_Client.lua (UIConfig section)
  • Add more commands in AdminSystem_Server.lua (Commands table)
  • Modify title appearance in TitleSystem_Client.lua (TitleConfig)
  • Adjust permissions in RankList
  • Change command prefix from ";" to anything


🛠️ ADVANCED MODIFICATIONS:

  • Add custom ranks (edit Ranks table)
  • Create command aliases
  • Add more UI actions
  • Integrate with game-specific features
  • Add discord webhook logging


═══════════════════════════════════════════════════════════════════════════════

                          🎮 ADMIN SYSTEM v1.0
                     Created with ❤️ for Roblox Developers
                            Professional Quality
                          Production-Ready Code

═══════════════════════════════════════════════════════════════════════════════
