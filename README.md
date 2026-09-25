# minecraft-at-school (read carfully)
how to play Minecraft with friends at school on strict networks (without teachers seeing your screen)
(there will be a lot of copy and pasting files to flash drive to put on school computer if you cant put files on school computer then try something else)


1.) go to any code editor, eg: https://liveweave.com/index.php, https://www.w3schools.com/html/tryit.asp?filename=tryhtml_basic, https://jsbin.com/?html,output, etc (the code editor needs to have html section) (visit on school computer)
 
2.) once you do that download the EaglercraftX 1.8.8 Offline file here (use any version of 1.8.8 as long as it is 1.8.8 because 1.8.8 has multiplayer and 1.12.2 does not)(you may need to copy the download file from another device to the school computer): https://eaglercraft.com/p/downloads (you may be able to stop here and run the .html file if it does not run continue with next steps)  

3.) once you do that go to the code editor you chose copy this code: 

<!DOCTYPE html>
<html>
<head>
    <title>HTML File Runner</title>
</head>
<body>

<h3>Upload HTML file to run</h3>

<input type="file" id="file" accept=".html,.htm">

<button onclick="runFile()">Run in about:blank</button>

<script>
function runFile() {
    const fileInput = document.getElementById("file");

    if (!fileInput.files.length) {
        alert("Pick an HTML file first");
        return;
    }

    const file = fileInput.files[0];
    const reader = new FileReader();

    reader.onload = function(e) {
        const code = e.target.result;

        const win = window.open("about:blank", "_blank");

        if (!win) {
            alert("Popup blocked");
            return;
        }

        win.document.open();
        win.document.write(code);
        win.document.close();
    };

    reader.readAsText(file);
}
</script>

</body>
</html> 

into the html section of the code editor you choose (you may need to press RUN depending on the code editor you used)

4.) upload the .html file into the running code by pressing the UPLOAD button

5.) press save button

6.) choose about:blank (teachers can't see screen) blob url (teachers can see screen) (I have only tested this on securely extension that lets teachers see your screen and cisco umbrella roaming client for blocking stuff at DNS level) 

7.) once you press launch it should open eaglercraft 1.8.8 in a new tab ( it may take a long time to load sometimes) (the game may lag depending on device)    

