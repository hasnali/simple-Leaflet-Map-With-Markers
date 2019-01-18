<h1>simple-Leaflet-Map-With-Markers</h1>
<p>
	<h3>Installation Steps</h3>
	<ol>
		<li>download the file and open it with web browser for test it</li>
		<li>you can change markers icon with your custom ones by changin red, green icons</li>
		<li>To Include in side Your Project : put these tow links in your code </li>
		<p>
			 <link rel="stylesheet" href="https://unpkg.com/leaflet@1.4.0/dist/leaflet.css" integrity="sha512-puBpdR0798OZvTTbP4A8Ix/l+A4dHDD0DGqYW6RQ+9jxkRFclaxxQb/SJAWZfWAkuyeQUytO7+7N4QKrDh+drA==" crossorigin="" />
    <script src="https://unpkg.com/leaflet@1.4.0/dist/leaflet.js" integrity="sha512-QVftwZFqvtRNi0ZyCtsznlKSWOStnDORoefr1enyq5mVL4tmKB3S/EnC3rRJcxCPavG10IcrVGSmPh6Qw5lwrg==" crossorigin=""></script>
		</p>
		<li>
		example:
		</li>
		<code>
			
				    
				    // here we set the center of the map.
				    var map = L.map('map').setView([35.092, 36.078], 7);
				    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
				        attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
				    }).addTo(map);

				    var LeafIcon = L.Icon.extend({
				        options: {
				            shadowUrl: 'leaf-shadow.png',
				            iconSize: [38, 95],
				            shadowSize: [50, 64],
				            iconAnchor: [22, 94],
				            shadowAnchor: [4, 62],
				            popupAnchor: [-3, -76]
				        }
				    });
				    // here we set the icons we can change them with other images.
				    var greenIcon = new LeafIcon({ iconUrl: 'leaf-green.png' }),
				        redIcon = new LeafIcon({ iconUrl: 'leaf-red.png' }),
				        orangeIcon = new LeafIcon({ iconUrl: 'leaf-orange.png' });
				    // first location.
				    L.marker([35.092619, 36.0781583], { icon: greenIcon }).bindPopup("First Loc").addTo(map);
				    // second location.
				    L.marker([35.537489, 35.8298193], { icon: redIcon }).bindPopup("Second Loc").addTo(map);
				    // third location.
				    L.marker([33.511745, 36.1934849], { icon: orangeIcon }).bindPopup("third Loc").addTo(map);
  			  
		</code>
	</ol>
</p>
