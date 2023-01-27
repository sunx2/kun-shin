![image](https://media.discordapp.net/attachments/275135052466094081/1068379305815576637/genshin-impact-banner-1-550x309.png)

## #Links
<table>
<tr><td> Base Game </td> <td> <a href="https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20221024103618_h2e3o3zijYKEqHnQ/GenshinImpact_3.2.0.zip" >[Download] </a></td> <tr>
<tr><td> Chinese Audio </td> <td> <a href="https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20221024103618_h2e3o3zijYKEqHnQ/Audio_Chinese_3.2.0.zip" >[Download] </a></td> <tr>
<tr><td> English Audio </td> <td> <a href="https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20221024103618_h2e3o3zijYKEqHnQ/Audio_English(US)_3.2.0.zip" >[Download] </a></td> <tr>
<tr><td> Korean Audio </td> <td> <a href="https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20221024103618_h2e3o3zijYKEqHnQ/Audio_Korean_3.2.0.zip" >[Download] </a></td> <tr>
<tr><td> Japanese Audio </td> <td> <a href="https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20221024103618_h2e3o3zijYKEqHnQ/Audio_Japanese_3.2.0.zip" >[Download] </a></td> <tr>
<tr><td> Patch</td> <td> <a href="https://mega.nz/file/o51FFaDJ#KrRm-df4O3z14t50d74pK5sZTYDrRGEjv_mTFHW0AV4" >[Download] </a></td> <tr>
<tr><td> Fiddler Classic </td> <td> <a href="https://mega.nz/file/U081HDgB#267UI5cc9MYVDdNYhpjE6GNCBHr_YVlcIq76dBJ8VHc" >[Download] </a></td> <tr>
</table>

<details>
<summary> <b>Steps to Install game</b> </summary>

## #Steps
<ol type = "1">
<li>Download and unpack the game.
</li>
<li>Download and unpack the patch on top of the game overwriting the original DLL file.</li>
<li> Download and unpack the desired voice pack to be used on the game.</li>
<li>Download and install <a href="https://mega.nz/file/U081HDgB#267UI5cc9MYVDdNYhpjE6GNCBHr_YVlcIq76dBJ8VHc">FIDDLER CLASSIC</a></li>
<li>Run fiddler and go on FiddlerScript tab, paste the following script then click Save Script:

```cs 
import System;
import System.Windows.Forms;
import Fiddler;
class Handlers
{
    static var redirect = [
        "://dispatchosglobal.yuanshen.com/",
        "://osusadispatch.yuanshen.com/",
        "://osasiadispatch.yuanshen.com/",
        "://oseurodispatch.yuanshen.com/",
        "://hk4e-sdk-os-static.hoyoverse.com/",
        "://sdk-os-static.hoyoverse.com/",
        "://api-account-os.hoyoverse.com/",
        "://hk4e-sdk-os.hoyoverse.com/",
        "://account.hoyoverse.com/?type=sdk"        
        ];
    static var block = [
        "://overseauspider.yuanshen.com:8888/log",
        "://log-upload-os.hoyoverse.com/sdk/dataUpload",
        "://log-upload.hoyoverse.com/sdk/dataUpload",
        "://minor-api-os.hoyoverse.com/common/h5log/log/batch",
        "://log-upload-os.hoyoverse.com/crash/dataUpload"        
        ];
    static var host = "omega.servegame.com";
    static var port = 7443;
    static var protocol = "https";
    static function OnBeforeRequest(o: Session)
    {
        for (var i = 0; i < block.length; ++i) {
            if (o.uriContains(block[i]))
            {
                o.oRequest.FailSession(404, "Blocked", "Oh no!!!");
                return;
            }
        }
        for (var i = 0; i < redirect.length; ++i) {
            if (o.uriContains(redirect[i])) {
                o.oRequest.headers.UriScheme = protocol;
                o.host = host;  
                o.port = port;
                break;
            }
        }
    }
}

```
</li>
<li> On Fiddler, go to Tools->Options->HTTPS and set everything as following

![image](https://media.discordapp.net/attachments/275135052466094081/1068382731542724608/image.png)</li>

<li>Press Win + R, write regedit.exe and then run it.
</li>
<li>Go to 

`
Computer\HKEY_CURRENT_USER\Software\miHoYo\Genshin Impact
`
on regedit</li>
<li> Select the GENERAL_DATA_h key, open it and find “deviceVoiceLanguageType”, the number following it is the current voice language on the game settings, 1 = English, 2 = Japanese, set the value accordingly to the voice pack language you downloaded and save it.
10- Run the game from the .exe file on the game folder
</li>
<li>Run the game from the .exe file on the game folder
</li>
<li>At login screen choose an hard to guess username, you do not use password (put anything on that field), so the only security of your account is having a hard to guess username (merge your password on it), the account will be automatically created on first login, then simply keep using the same username afterwards to access the same account.
</li>
</ol>

</details>

<details>
<summary> <strong> Changes to base game.</strong> </summary>

### ⭐ limited Time Gear
<span style="font-size:14px">
Pets, Gadgets, Weapons, Furnishings, Blueprints, Skins, Wings. All the old retired Event items can be bought or found in the game somewhere. Changelog shows exact locations.
</span>

### ⭐ Wishes Overhaul 😍
<span style="font-size:14px">
 Fates now cost <strong style="font-size:18px">10 Primogem per roll.</strong> In addition, almost every instance of getting <b>rewarded Fates now gives you 5x or 10x more (Adventurer Ranks, Quests, Offering Systems, Character Ascensions)</b>
</span>

### ⭐ Banner Overhaul 
<span style="font-size:14px">
There are a total of<b> 7 Banners running</b>. Four of the Banners (Klee, Xiao, Arataki Itto, and Tighnari) will ONLY drop characters from that City (Mondstadt, Liyue, Inazuma and Sumeru). Wanderlust Invocation can now drop every single character available (Except Traveler and Aloy). The two Weapon Banners can drop any available weapons. The featured Characters on the Banner drop less often than normal as well.
</span>


### ⭐ Banner Probability Overhaul 
<span style="font-size:14px">
Banner Probability Overhaul: Character Banners will only drop 3 Star Weapons, 4 Star Characters and 5 Star Characters. Weapon Banners will only drop 3/4/5 Star Weapons. In addition, 4/5 Stars will drop more often and the Pity System activates at 50 rolls instead of 74.
</span>

### ⭐ Banner Probability Overhaul 
<span style="font-size:14px">
Banner Probability Overhaul: Character Banners will only drop 3 Star Weapons, 4 Star Characters and 5 Star Characters. Weapon Banners will only drop 3/4/5 Star Weapons. In addition, 4/5 Stars will drop more often and the Pity System activates at 50 rolls instead of 74.
</span>

### 🫖 Teapot Overhaul 
<span style="font-size:14px">
Furnishing Crafting changed to be much faster (4hr>8min, 6hr>12min, 8hr>16min, 10hr>20min, 12hr>24min, 14hr>28min, 16hr>32min) and can be immediately finished with an 'Vial of Adeptal Speed'. Farming is faster as well (30min vs 2 days). Most important items have had their limited purchase removed in Realm Depot. You also get more Companionship EXP and Realm Currency per hour (5x normal amount per level).
</span>
### 🔎 Gadget Changes 
<span style="font-size:14px">
Gadget Changes: All four Resonance Stones have had their hint AOE on the map shrunk so they're easier to use when you're completing the Statues of the Seven. Parametric Transformer also now recharges in 6 Hours instead of 6 Days.
</span>

#### 💫 Each one will now reward you with the Refining Material for any Event Weapons you purchase in that zone. At max level you also get a free 5 Star Character for that specific zones Archon. Frostbearing Tree and Lumenstone Adjuvant also follow this pattern.

- **Statue of the Seven (Anemo)**: 4x 'The Visible Wings', 4x 'Fragments of Innocence',  Character 'Venti'
- **Statue of the Seven (Geo)**: 4x 'Emperor's Balsam', Character 'Zhongli'
- **Statue of the Seven (Electro)**: 4x 'Glowing Gem', Character 'Raiden Shogun'
- **Statue of the Seven (Dendro)**: 4x 'Plume of the Changing Winds', Character 'Nahida'
- **Frostbearing Tree**: 4x 'Festering Dragon Marrow', 4x 'Alkahest', Character 'Albedo'
- **Lumenstone Adjuvant**: Weapon 'Oathsworn Eye', 4x 'Ointment of Sight', Characters 'Keqing' and 'Xiao'

#### 🏠 Hangouts: All Hangouts now give the Character featured in the Hangout when you complete all endings

- Barbara (4) - Wellspring of Healing
- Chongyun (4) - Signs of Evil
- Noelle (4) - Chivalric Training
- Bennett (4) - Fantastic Voyage
- Noelle (4) - Knightly Exam Prep
- Diona (4) - The Cat and the Cocktail
- Thoma (4) - A Housekeeper's Daily Chores
- Sayu (4) - Yoohoo Art: Seichou no Jutsu
- Beidou (4) - When the Crux Shines Bright
- Gorou (4) - The Canine General's Special Operations
- Ningguang (4) - The Jade Chamber's Returning Guest
- Yun Jin (4) - A Song That Knows Grace
- Kuki Shinobu (4) - The Gang's Daily Deeds
- Shikanoin Heizou (4) - Trap 'Em by Storm

#### 📕 Story Arcs: All Story Quests now give the Character featured in the Arc (4 Star) or a Stella Fortuna (5 Star) on final quest of the Arc.

- Razor (4) - Fate's Chosen Lupical
- Kaeya (4) - Kaeya's Gain
- Diluc (5) - Darknight Hero's Alibi
- Amber (4) - Outrider Style
- Jean (5) - Master's Day Off
- Lisa (4) - Lost Book
- Venti (5) - Should You Be Trapped in a Windless Land
- Eula (5) - Through the Motions, to the Heart
- Klee (5) - A Very Volatile Treasure
- Mona (5) - A Bewildering Fate
- Xiangling (4) - Cooking Showdown
- Tartaglia (5) - Defender of Childhood Dreams
- Zhongli (5) - A Record of All Things
- Yelan (5) - Foregone Conclusion
- Ganyu (5) - A Pact That Crosses Time
- Albedo (5) - The Final Experiment: Withering Glory
- Xiao (5) - Insights of Drifting Dreams
- Hu Tao (5) - Perfect Send-Off
- Zhongli (5) - Amidst Chaos, the Rock Is Unmoved
- Xingqiu (4) - Justice Is Its Own Reward
- Kamisato Ayaka (5) - With You
- Yoimiya (5) - Together Under the Fireworks
- Raiden Shogun (5) - To Hear Mortal Hearts
- Sangonomiya Kokomi (5) - New Beginning
- Arataki Itto (5) - The Oni's Pride
- Yae Miko (5) - Banquet of Parting
- Kamisato Ayato (5) - The Wind Settles
- Raiden Shogun (5) - Radiant Sakura
- Kaedehara Kazuha (5) - Ere the End, a Glance Back
- Tighnari (5) - Garden Memories
- Nilou (5) - The Reason We Are Gathered Here
- Cyno (5) - All Returns to Silence
- Nahida (5) - Dream of Farewell


#### 🎣 Fishing Overhaul:

 Added new Weapons, Gadgets and Characters to be purchased from the Angler Shops. In addition, Fishing Points now have 50 fishes instead of the normal ~10 before being exhausted.


#### 🛒 Paimon Shop: 
 Added permanent line-up of Characters to purchase (Kaeya, Lisa, Amber, Barbara, Xinyan, and Aloy), Royal Weapons and Blackcliff Weapons can be maxed out. Most purchase limits have been removed as well.

#### 🛍️ Shop Limits Removed:
 Food Ingredients and other limited purchase items from normal shops have been removed from some. For the rarer items like Cor Lapis you spend both Mora and Resin to purchase them. (EX: Cor Lapis costs 4 Resin per 1)

#### 😊 Limited Items Added:
 Normally Limited Items like Crowns of Insight and Fates can be purchased from certain areas in unlimited supply if you really want to farm forever.

#### 🌙 Resin Overhaul:
 Resin now caps and regenerates to 240 Resin. In addition, instead of 1 Resin every 8 Minutes it's 1 Resin every 1 Minute. Purchasing Resin with Primogems now stays at the cost of 50 and doesn't increase.

#### 💰Resin Cost Removal:
 Ley Lines, Domains and Weekly Bosses have had their Resin cost changed to 1. Farm them as much as you want.


#### ⌚ Time Gate Removal:
 Weekly Bosses can be run 99 times per week now. Domains are now in 24/7 Sunday mode so you can pick whichever one you want on any day. Crimson Wishes now give 10x Crimson Agates instead of 1x, so you can finish the Frostbearing Tree when Crimson Wishes are unlocked.

#### 📆 Daily Commissions:
 Every Daily Commission gives you 10x Story Keys and you can now hold 99 Story Keys, removing them as a Time Gate. You also now get 63 Character Ascension Material when you claim your Adventure Treasure Pack per day.

#### 🌪️Spiral Abyss: 
Set up schedule so it should last to '2030-01-01'.

#### 🏙️ Reputation Overhaul:
 When you get to rank 4 and rank 8 for that zones Reputation you get rewarded characters. In addition, tweaked EXP given so that you should only have to complete 'World Completion' and 'City Quests' to fully max out your Reputation. No need to farm Bounties.

- Mondstadt: LV4 Bennett, LV8 Jean
- Liyue: LV4 Xinyan, LV8 Qiqi
- Inazuma: LV4 Kujou Sara, LV8 Kaedehara Kazuha
- Sumeru: LV4 Candace, LV8 Nilou


# 😄 Enjoy 😄
</details>
