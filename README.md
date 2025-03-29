<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Les Chouchous des Managers</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #ffccd5;
            padding: 20px;
            text-align: center;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        header img {
            height: 50px;
            margin-right: 10px;
        }
        main {
            padding: 20px;
        }
        .definition {
            background-color: #cce7ff;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 20px;
        }
        .manager-section {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin-bottom: 20px;
        }
        .manager {
            text-align: center;
            margin-bottom: 20px;
        }
        .manager img {
            border-radius: 50%;
            width: 100px;
            height: 100px;
            object-fit: cover;
        }
        .manager h3 {
            margin-top: 10px;
        }
        .favorite-button {
            background-color: #ffb3c1;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
        }
        .dropdown {
            position: relative;
            display: inline-block;
        }
        .dropdown-content {
            display: none;
            position: absolute;
            background-color: #fff;
            min-width: 200px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1;
            border-radius: 8px;
            overflow: hidden;
        }
        .dropdown-content div {
            padding: 10px;
            cursor: pointer;
        }
        .dropdown-content div:hover {
            background-color: #f1f1f1;
        }
        .dropdown-content .add-button {
            color: red;
            font-weight: bold;
        }
        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
        }
        .popup.show {
            display: block;
        }
        .popup-close {
            background: none;
            border: none;
            font-size: 16px;
            cursor: pointer;
        }
        .collaborator {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
        }
        .collaborator img {
            border-radius: 50%;
            width: 50px;
            height: 50px;
            object-fit: cover;
            margin-right: 10px;
        }
        .qualities-button {
            background-color: #cce7ff;
            border: none;
            padding: 5px 10px;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <img src="https://www.fr-dba.com/wp-content/uploads/2020/11/logo-dba-vf-1.png" alt="Logo DBA">
        <h1>Les Chouchous des Managers</h1>
    </header>
    <main>
        <div class="definition">
            <h2>Définition de Chouchou</h2>
            <p>Un chouchou est une personne ou une chose qui est particulièrement appréciée ou préférée par quelqu'un. Ce terme affectueux est souvent utilisé pour désigner les favoris dans divers contextes.</p>
        </div>
        <div class="manager-section">
            <div class="manager">
                <img src="https://media.licdn.com/dms/image/v2/C4D03AQGsE6Fv_OQmMQ/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1540125746107?e=1748476800&v=beta&t=oybW8-m8CFChiyNwlpdVnNWnzUaMttJo8fjK3yPCyvo" alt="Manager Benoit">
                <h3>Benoit</h3>
                <div class="dropdown">
                    <button class="favorite-button">Voir les Chouchous</button>
                    <div class="dropdown-content">
                        <div class="collaborator">
                            <img src="https://media.licdn.com/dms/image/v2/C4D03AQGjPIXw8SQjpQ/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1646234300085?e=1748476800&v=beta&t=MDXOTK7PoPIwgWfQKZXRdNp1pPDJCmbSbIUOmTnthNQ" alt="Gautier">
                            <span>Gautier</span>
                            <button class="qualities-button" onclick="showQualities('Gautier')">Qualités & Défauts</button>
                        </div>
                        <div class="collaborator">
                            <img src="https://media.licdn.com/dms/image/v2/D4E03AQGKEtgdV2XYuQ/profile-displayphoto-shrink_100_100/profile-displayphoto-shrink_100_100/0/1689058193134?e=1748476800&v=beta&t=7-iwPgY2x-FAwvJ5FbTA-Ozo1p9VSTsB9FYgq9v7q6Q" alt="Joffray">
                            <span>Joffray</span>
                            <button class="qualities-button" onclick="showQualities('Joffray')">Qualités & Défauts</button>
                        </div>
                        <div class="add-button" onclick="showAddPopup()">Ajouter un Chouchou</div>
                    </div>
                </div>
            </div>
            <div class="manager">
                <img src="https://media.licdn.com/dms/image/v2/C5603AQFOT57GvjYZaA/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1517053081934?e=1748476800&v=beta&t=DAx2WaBZehwcDDUGm7m6D578ksUvVwHiX0KlhBOl4NM" alt="Manager Audrey">
                <h3>Audrey</h3>
                <div class="dropdown">
                    <button class="favorite-button">Voir les Chouchous</button>
                    <div class="dropdown-content">
                        <div>En raison d'une indisponibilité, son classement est indisponible pour le moment.</div>
                        <div class="add-button" onclick="showAddPopup()">Ajouter un Chouchou</div>
                    </div>
                </div>
            </div>
            <div class="manager">
                <img src="https://media.licdn.com/dms/image/v2/C4D03AQEISt7mKRzUdQ/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1539187124432?e=1748476800&v=beta&t=Z6mPEZe7DRpRB2T7XeP1Au1imwfzUxnduba_AE26YqM" alt="Manager Dan">
                <h3>Dan</h3>
                <div class="dropdown">
                    <button class="favorite-button">Voir les Chouchous</button>
                    <div class="dropdown-content">
                        <div>Chouchou 1 de Dan: Description du chouchou 1 de Dan.</div>
                        <div>Chouchou 2 de Dan: Description du chouchou 2 de Dan.</div>
                        <div class="add-button" onclick="showAddPopup()">Ajouter un Chouchou</div>
                    </div>
                </div>
            </div>
            <div class="manager">
                <img src="https://media.licdn.com/dms/image/v2/C5603AQG-Gryr95xBAg/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1541498116747?e=1748476800&v=beta&t=2X3ZbITi7rN6sdChkDUK_rCwwJxldmnjHurr2Xhdb68" alt="Manager Alimath">
                <h3>Alimath</h3>
                <div class="dropdown">
                    <button class="favorite-button">Voir les Chouchous</button>
                    <div class="dropdown-content">
                        <div>Pas de chouchou, elle adore tout le monde.</div>
                        <div class="add-button" onclick="showAddPopup()">Ajouter un Chouchou</div>
                    </div>
                </div>
            </div>
        </div>
        <div class="popup" id="add-popup">
            <div class="popup-content">
                <p>T'as cru t'allais pouvoir t'ajouter en chouchou comme ça ? Espèce de fou ! Au boulot.</p>
            </div>
            <button class="popup-close" onclick="hideAddPopup()">Fermer</button>
        </div>
        <div class="popup" id="qualities-popup">
            <div class="popup-content">
                <h3 id="qualities-title"></h3>
                <p id="qualities-text"></p>
            </div>
            <button class="popup-close" onclick="hideQualitiesPopup()">Fermer</button>
        </div>
    </main>
    <script>
        let currentDropdown = null;

        function toggleDropdown(manager) {
            const dropdownContent = document.querySelector(`.manager:has(> img[alt='Manager ${manager}']) .dropdown-content`);
            if (currentDropdown && currentDropdown !== dropdownContent) {
                currentDropdown.style.display = 'none';
            }
            dropdownContent.style.display = dropdownContent.style.display === 'block' ? 'none' : 'block';
            currentDropdown = dropdownContent;
        }

        function showAddPopup() {
            document.getElementById('add-popup').classList.add('show');
        }

        function hideAddPopup() {
            document.getElementById('add-popup').classList.remove('show');
        }

        function showQualities(name) {
            const title = document.getElementById('qualities-title');
            const text = document.getElementById('qualities-text');
            title.textContent = `${name}'s Qualités & Défauts`;
            text.textContent = `Voici les qualités et défauts de ${name}.`;
            document.getElementById('qualities-popup').classList.add('show');
        }

        function hideQualitiesPopup() {
            document.getElementById('qualities-popup').classList.remove('show');
        }

        document.querySelectorAll('.dropdown').forEach(dropdown => {
            dropdown.addEventListener('click', function(event) {
                if (event.target.tagName === 'BUTTON') {
                    toggleDropdown(event.target.closest('.manager').querySelector('h3').textContent);
                }
            });
        });

        window.onclick = function(event) {
            if (!event.target.matches('.favorite-button')) {
                const dropdowns = document.querySelectorAll('.dropdown-content');
                dropdowns.forEach(dropdown => {
                    if (dropdown.style.display === 'block') {
                        dropdown.style.display = 'none';
                    }
                });
                currentDropdown = null;
            }
        }
    </script>
</body>
</html>
