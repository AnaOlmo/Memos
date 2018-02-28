---


---

<p>MEMO CORDOVA</p>
<h2 id="les-commandes-cordova">Les commandes Cordova</h2>

<table>
<thead>
<tr>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>cordova create <path></path></td>
<td>$ npm install -g cordova</td>
</tr>
<tr>
<td>cordova platform add </td>
<td>$ cd MyApp et $ cordova platform add browser /add android</td>
</tr>
<tr>
<td>Si erreur “command not found” avec CD MyApp</td>
<td>1.  Click on the <strong>Start</strong> menu in the lower-left corner of the desktop 2.  In the search bar, search for <strong>Environment Variables</strong> and select <strong>Edit the system Environment Variables</strong> from the options that appear 3.  In the window that appears, click the <strong>Environment Variables</strong> button ##### To create a new environment variable:[] (<a href="http://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html#to-create-a-new-environment-variable">http://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html#to-create-a-new-environment-variable</a>) 1.  Click <strong>New…</strong> and enter the variable name and value ##### To set your <strong>PATH</strong>:<a href="http://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html#to-set-your-path"></a> 1.  Select the <strong>PATH</strong> variable and press <strong>Edit</strong>. 2.  Add entries for the relevant locations to the <strong>PATH</strong> (c:/users/anaolmo/roaming/npm), move up.</td>
</tr>
<tr>
<td>cordova run </td>
<td>$ cordova run browser et $ cordova run android</td>
</tr>
<tr>
<td>cordova plugin add </td>
<td>exemple $ cordova plugin add cordova-plugin-camera</td>
</tr>
</tbody>
</table><h2 id="structure-d’un-projet-cordova">Structure d’un projet Cordova</h2>

<table>
<thead>
<tr>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>Contenu du répertoire “platforms”</td>
<td>dossiers Android et Browser et sous dossiers Gradle / JSON</td>
</tr>
<tr>
<td>Contenu du répertoire “plugins”</td>
<td>Fichiers JSON: Android-Fetch-Browser et Cordova plugin whitelist</td>
</tr>
<tr>
<td>Contenu du répertoire “www”</td>
<td>CSS-Images-JS-Index.html</td>
</tr>
<tr>
<td>Contenu du fichier “package.json”</td>
<td>liste les dépendances du projet, spécifie la version du package.</td>
</tr>
<tr>
<td>Contenu du fichier “config.xml”</td>
<td>Un fichier XML est un fichier texte utilisant des balises pour l’échange de données automatisés entre systèmes.</td>
</tr>
<tr>
<td>Contenu du fichier “www/index.html”</td>
<td>contient la vue du browser</td>
</tr>
</tbody>
</table>
