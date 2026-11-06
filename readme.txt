DayZ Chinook Added To Heli Crash Events Mod Files For Console and PC Community Servers Instructions & Terms Of Use

When installed correctly these files will add Chinooks, and all varients of helicopter crashes, to Chernarus, Livonia (Enoch) & Sakhal Maps. (Nasdara already has Chinooks in a seperate event.)

Limited Testing on PC Chernarus, Livonia & Sakhal Local Server, DAYZ Version 1.30 Nov 26.

Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Stop your server.



Upload all the file veh-more-HeliCrash-events.xml  from the extracted folder to inside the "custom" folder of the mission directory on your server.
(If you haven't got a "custom" folder, create one.)

Next open up your vanilla cfgeconomycore.xml, and near the bottom, above the closing

</economycore>

tag,

paste this:

	<ce folder="custom">
	<file name="veh-more-HeliCrash-events.xml" type="events" />
	</ce>

If you are already using files to append your vanilla mission files, it should look something like this:

<ce folder="custom">
	<file name="some-other-types-file.xml" type="types" />
	<file name="some-other-events.xml" type="events" />
	<file name="veh-more-HeliCrash-events.xml" type="events" />
	<file name="some-other-messages.xml" type="messages" />
	<file name="some-other-globals.xml" type="globals" />
	</ce>

Save the file.

Upload where necessary.

Next we need to add the mapgroupproto.xml entries, so that the server knows where to spawn the loot on the crashes.

Open up your mapgroupproto.xml and copy and paste the following code, near the top, below 	</defaults>

<!-- extra heli crash entries, may be duplicates -->

		<group name="StaticObj_Wreck_Mi24_TK_DE" lootmax="15">
				<usage name="Military" />
				<container name="lootFloor" lootmax="15">
						<category name="containers" />
						<category name="weapons" />
						<tag name="floor" />
						<tag name="shelves" />
						<tag name="ground" />
						<point pos="3.199696 0.010132 -0.840539" range="1.110352" height="2.000000" flags="32" />
						<point pos="6.250588 0.017426 -2.432528" range="1.200000" height="2.000000" flags="32" />
						<point pos="9.127810 0.037888 -2.385160" range="1.200000" height="2.000000" flags="32" />
						<point pos="11.438901 0.059601 -1.463723" range="1.200000" height="2.000000" flags="32" />
						<point pos="10.291038 0.070816 1.903448" range="1.200000" height="2.000000" flags="32" />
						<point pos="7.498953 0.062866 3.395692" range="1.200000" height="2.000000" flags="32" />
						<point pos="3.825542 0.051086 4.384155" range="1.200000" height="2.000000" flags="32" />
						<point pos="-0.157418 0.027222 4.226594" range="1.200000" height="2.000000" flags="32" />
						<point pos="-3.453436 0.007523 3.086862" range="1.200000" height="2.000000" flags="32" />
						<point pos="-6.722156 -0.003494 3.566299" range="1.200000" height="2.000000" flags="32" />
						<point pos="-8.399441 -0.029114 1.175172" range="1.200000" height="2.000000" flags="32" />
						<point pos="-6.137133 -0.040222 -1.051637" range="1.200000" height="2.000000" flags="32" />
						<point pos="-3.527979 -0.041580 -2.383079" range="1.200000" height="2.000000" flags="32" />
						<point pos="-2.690195 -0.059601 -4.953552" range="1.200000" height="2.000000" flags="32" />
						<point pos="0.551658 -0.054047 -6.434073" range="1.200000" height="2.000000" flags="32" />
						<point pos="3.638502 -0.016998 -5.085208" range="1.041325" height="2.000000" flags="32" />
				</container>
		</group>
		<group name="StaticObj_Wreck_Chinook_DE" lootmax="15">
				<usage name="Military" />
				<container name="lootFloor" lootmax="15">
						<category name="containers" />
						<category name="clothes" />
						<category name="weapons" />
						<tag name="floor" />
						<tag name="shelves" />
						<tag name="ground" />
						<point pos="8.906539 0.000000 2.512233" range="0.530948" height="2.000000" flags="32" />
						<point pos="8.103426 0.000000 4.045586" range="1.200000" height="2.000000" flags="32" />
						<point pos="0.673840 0.000000 2.806289" range="1.200000" height="2.000000" flags="32" />
						<point pos="-1.292189 0.000000 2.531386" range="0.785155" height="0.189270" flags="32" />
						<point pos="2.946334 0.000000 2.737701" range="1.073530" height="2.000000" flags="32" />
						<point pos="4.952571 0.000000 2.533124" range="0.916016" height="2.000000" flags="32" />
						<point pos="7.234792 0.000000 1.972001" range="0.667747" height="1.669367" flags="32" />
						<point pos="8.570404 0.000000 0.458071" range="1.200000" height="2.000000" flags="32" />
						<point pos="8.164338 0.000000 -1.281064" range="0.585910" height="1.937805" flags="32" />
						<point pos="6.978744 0.000000 -2.978269" range="1.200000" height="2.000000" flags="32" />
						<point pos="5.019855 0.000000 -3.207403" range="0.772243" height="2.000000" flags="32" />
						<point pos="3.030727 0.000000 -3.227721" range="1.200000" height="2.000000" flags="32" />
						<point pos="1.282537 0.000000 -2.961828" range="0.568294" height="2.000000" flags="32" />
						<point pos="-0.708475 0.000000 -2.918092" range="1.200000" height="2.000000" flags="32" />
						<point pos="-3.142881 0.000000 -2.893627" range="0.779613" height="1.949033" flags="32" />
						<point pos="-5.114168 0.000000 -2.573234" range="1.200000" height="2.000000" flags="32" />
						<point pos="-7.293026 0.000000 -1.379689" range="1.200000" height="2.000000" flags="32" />
						<point pos="-7.821355 0.000000 0.280199" range="0.541941" height="2.000000" flags="32" />
						<point pos="-7.140625 0.000000 1.594225" range="0.937943" height="2.000000" flags="32" />
						<point pos="-6.097542 0.000000 3.173330" range="0.954567" height="2.000000" flags="32" />
						<point pos="-4.529471 0.000000 4.046666" range="0.840303" height="2.000000" flags="32" />
						<point pos="-2.395017 0.000000 4.932273" range="1.200000" height="2.000000" flags="32" />
						<point pos="-0.267683 0.000000 5.672090" range="1.052305" height="2.000000" flags="32" />
						<point pos="1.882588 0.000000 5.541307" range="1.101940" height="2.000000" flags="32" />
						<point pos="4.071617 0.000000 5.550753" range="1.087110" height="2.000000" flags="32" />
						<point pos="6.065507 0.000000 5.160886" range="0.944539" height="2.000000" flags="32" />
						<point pos="-3.516180 0.574554 0.208568" range="0.443750" height="1.109375" />
						<point pos="-1.219945 0.538483 0.504462" range="0.594727" height="1.486819" />
						<point pos="1.236836 0.648987 0.799685" range="0.271875" height="0.679688" />
						<point pos="3.294142 0.788330 -0.736208" range="0.271875" height="0.679688" />
						<point pos="2.882787 0.558105 0.076852" range="0.667956" height="0.166962" />
						<point pos="5.223816 0.506104 0.106962" range="0.375000" height="0.937439" />
				</container>
		</group>
		
		<!-- end of extra heli crash loot entries-->
	
Save the file.

Upload where necessary.
	
Vailidate your edited files to check you haven't made any mistakes with https://www.xmlvalidation.com/

Restart your server & changes should start to take effect.

----------

Dominus vobiscum! scalespeeder

GOOD LUCK!
