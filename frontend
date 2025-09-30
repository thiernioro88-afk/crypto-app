<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CryptoVault - Chiffrement de données sécurisé</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #34495e;
            --success-color: #2ecc71;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a3a, #2c3e50);
            color: var(--light-color);
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        h1 {
            color: var(--secondary-color);
            margin-bottom: 10px;
            font-size: 2.5rem;
        }
        
        .subtitle {
            color: var(--light-color);
            opacity: 0.8;
            font-size: 1.1rem;
        }
        
        .security-notice {
            background-color: rgba(52, 152, 219, 0.2);
            border-left: 4px solid var(--secondary-color);
            padding: 15px;
            margin-bottom: 25px;
            border-radius: 0 8px 8px 0;
        }
        
        .app-section {
            margin-bottom: 30px;
        }
        
        h2 {
            color: var(--secondary-color);
            margin-bottom: 15px;
            font-size: 1.5rem;
        }
        
        .input-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }
        
        textarea, input[type="password"], input[type="text"] {
            width: 100%;
            padding: 12px 15px;
            background-color: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 8px;
            color: var(--light-color);
            font-size: 1rem;
            resize: vertical;
            transition: all 0.3s ease;
        }
        
        textarea:focus, input:focus {
            outline: none;
            border-color: var(--secondary-color);
            box-shadow: 0 0 0 2px rgba(52, 152, 219, 0.2);
        }
        
        .btn-group {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 12px 20px;
            background-color: var(--secondary-color);
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 140px;
        }
        
        button:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }
        
        button.secondary {
            background-color: var(--dark-color);
        }
        
        button.secondary:hover {
            background-color: #2c3e50;
        }
        
        button.danger {
            background-color: var(--accent-color);
        }
        
        button.danger:hover {
            background-color: #c0392b;
        }
        
        .result {
            margin-top: 20px;
            padding: 15px;
            border-radius: 8px;
            background-color: rgba(255, 255, 255, 0.05);
            display: none;
        }
        
        .result.visible {
            display: block;
        }
        
        .result h3 {
            margin-bottom: 10px;
            color: var(--success-color);
        }
        
        .copy-btn {
            margin-top: 10px;
            background-color: var(--success-color);
        }
        
        .copy-btn:hover {
            background-color: #27ae60;
        }
        
        .algo-selector {
            display: flex;
            gap: 15px;
            margin-bottom: 20px;
        }
        
        .algo-option {
            flex: 1;
            text-align: center;
            padding: 15px;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }
        
        .algo-option.selected {
            border-color: var(--secondary-color);
            background-color: rgba(52, 152, 219, 0.1);
        }
        
        .algo-option h4 {
            margin-bottom: 5px;
            color: var(--secondary-color);
        }
        
        .algo-desc {
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            opacity: 0.7;
        }
        
        @media (max-width: 600px) {
            .container {
                padding: 20px;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .algo-selector {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>CryptoVault</h1>
            <p class="subtitle">Chiffrement de données sécurisé - 100% local</p>
        </header>
        
        <div class="security-notice">
            <p><strong>🔒 Sécurité maximale :</strong> Toutes les opérations de chiffrement/déchiffrement s'effectuent directement dans votre navigateur. Aucune donnée n'est envoyée à un serveur.</p>
        </div>
        
        <div class="app-section">
            <h2>Configuration du chiffrement</h2>
            
            <div class="algo-selector">
                <div class="algo-option selected" data-algo="AES-GCM">
                    <h4>AES-GCM</h4>
                    <p class="algo-desc">Recommandé - Authentifié</p>
                </div>
                <div class="algo-option" data-algo="AES-CBC">
                    <h4>AES-CBC</h4>
                    <p class="algo-desc">Standard - Sécurisé</p>
                </div>
            </div>
            
            <div class="input-group">
                <label for="password">Mot de passe de chiffrement :</label>
                <input type="password" id="password" placeholder="Entrez un mot de passe fort">
            </div>
            
            <div class="input-group">
                <label for="data-input">Données à chiffrer :</label>
                <textarea id="data-input" rows="5" placeholder="Entrez le texte que vous souhaitez chiffrer..."></textarea>
            </div>
            
            <div class="btn-group">
                <button id="encrypt-btn">Chiffrer les données</button>
                <button id="decrypt-btn" class="secondary">Déchiffrer des données</button>
                <button id="clear-btn" class="danger">Tout effacer</button>
            </div>
        </div>
        
        <div class="result" id="encrypted-result">
            <h3>Données chiffrées :</h3>
            <textarea id="encrypted-output" rows="4" readonly></textarea>
            <button class="copy-btn" id="copy-encrypted">Copier le résultat</button>
        </div>
        
        <div class="result" id="decrypted-result">
            <h3>Données déchiffrées :</h3>
            <textarea id="decrypted-output" rows="4" readonly></textarea>
            <button class="copy-btn" id="copy-decrypted">Copier le résultat</button>
        </div>
        
        <footer>
            <p>Développé avec ❤ pour protéger votre vie privée | CryptoVault v1.0</p>
        </footer>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Éléments DOM
            const passwordInput = document.getElementById('password');
            const dataInput = document.getElementById('data-input');
            const encryptBtn = document.getElementById('encrypt-btn');
            const decryptBtn = document.getElementById('decrypt-btn');
            const clearBtn = document.getElementById('clear-btn');
            const encryptedResult = document.getElementById('encrypted-result');
            const decryptedResult = document.getElementById('decrypted-result');
            const encryptedOutput = document.getElementById('encrypted-output');
            const decryptedOutput = document.getElementById('decrypted-output');
            const copyEncryptedBtn = document.getElementById('copy-encrypted');
            const copyDecryptedBtn = document.getElementById('copy-decrypted');
            const algoOptions = document.querySelectorAll('.algo-option');
            
            let selectedAlgorithm = 'AES-GCM';
            
            // Sélection de l'algorithme
            algoOptions.forEach(option => {
                option.addEventListener('click', function() {
                    algoOptions.forEach(opt => opt.classList.remove('selected'));
                    this.classList.add('selected');
                    selectedAlgorithm = this.getAttribute('data-algo');
                });
            });
            
            // Fonction pour dériver une clé à partir d'un mot de passe
            async function deriveKey(password, salt) {
                const encoder = new TextEncoder();
                const keyMaterial = await window.crypto.subtle.importKey(
                    "raw",
                    encoder.encode(password),
                    { name: "PBKDF2" },
                    false,
                    ["deriveKey"]
                );
                
                return await window.crypto.subtle.deriveKey(
                    {
                        name: "PBKDF2",
                        salt: salt,
                        iterations: 100000,
                        hash: "SHA-256"
                    },
                    keyMaterial,
                    { name: selectedAlgorithm, length: 256 },
                    false,
                    ["encrypt", "decrypt"]
                );
            }
            
            // Fonction de chiffrement
            async function encryptData() {
                const password = passwordInput.value;
                const data = dataInput.value;
                
                if (!password || !data) {
                    alert("Veuillez entrer un mot de passe et des données à chiffrer.");
                    return;
                }
                
                try {
                    const encoder = new TextEncoder();
                    const dataBuffer = encoder.encode(data);
                    
                    // Générer un sel et un vecteur d'initialisation (IV)
                    const salt = window.crypto.getRandomValues(new Uint8Array(16));
                    const iv = window.crypto.getRandomValues(new Uint8Array(12)); // 12 bytes pour AES-GCM
                    
                    // Dériver la clé
                    const key = await deriveKey(password, salt);
                    
                    // Chiffrer les données
                    const encryptedData = await window.crypto.subtle.encrypt(
                        {
                            name: selectedAlgorithm,
                            iv: iv
                        },
                        key,
                        dataBuffer
                    );
                    
                    // Combiner le sel, l'IV et les données chiffrées
                    const combined = new Uint8Array(salt.length + iv.length + encryptedData.byteLength);
                    combined.set(salt, 0);
                    combined.set(iv, salt.length);
                    combined.set(new Uint8Array(encryptedData), salt.length + iv.length);
                    
                    // Convertir en base64 pour l'affichage
                    const base64 = btoa(String.fromCharCode(...combined));
                    
                    // Afficher le résultat
                    encryptedOutput.value = base64;
                    encryptedResult.classList.add('visible');
                    decryptedResult.classList.remove('visible');
                    
                } catch (error) {
                    console.error("Erreur de chiffrement:", error);
                    alert("Une erreur s'est produite lors du chiffrement. Vérifiez votre navigateur prend en charge Web Crypto API.");
                }
            }
            
            // Fonction de déchiffrement
            async function decryptData() {
                const password = passwordInput.value;
                const encryptedData = dataInput.value;
                
                if (!password || !encryptedData) {
                    alert("Veuillez entrer un mot de passe et des données chiffrées.");
                    return;
                }
                
                try {
                    // Convertir de base64 à Uint8Array
                    const binaryString = atob(encryptedData);
                    const combined = new Uint8Array(binaryString.length);
                    for (let i = 0; i < binaryString.length; i++) {
                        combined[i] = binaryString.charCodeAt(i);
                    }
                    
                    // Extraire le sel, l'IV et les données chiffrées
                    const salt = combined.slice(0, 16);
                    const iv = combined.slice(16, 28); // 12 bytes pour AES-GCM
                    const data = combined.slice(28);
                    
                    // Dériver la clé
                    const key = await deriveKey(password, salt);
                    
                    // Déchiffrer les données
                    const decryptedData = await window.crypto.subtle.decrypt(
                        {
                            name: selectedAlgorithm,
                            iv: iv
                        },
                        key,
                        data
                    );
                    
                    // Convertir en texte
                    const decoder = new TextDecoder();
                    const decryptedText = decoder.decode(decryptedData);
                    
                    // Afficher le résultat
                    decryptedOutput.value = decryptedText;
                    decryptedResult.classList.add('visible');
                    encryptedResult.classList.remove('visible');
                    
                } catch (error) {
                    console.error("Erreur de déchiffrement:", error);
                    alert("Erreur de déchiffrement. Vérifiez le mot de passe et les données chiffrées.");
                }
            }
            
            // Fonction pour effacer tout
            function clearAll() {
                passwordInput.value = '';
                dataInput.value = '';
                encryptedOutput.value = '';
                decryptedOutput.value = '';
                encryptedResult.classList.remove('visible');
                decryptedResult.classList.remove('visible');
            }
            
            // Fonctions de copie
            function copyToClipboard(textareaId) {
                const textarea = document.getElementById(textareaId);
                textarea.select();
                document.execCommand('copy');
                alert('Copié dans le presse-papier !');
            }
            
            // Événements
            encryptBtn.addEventListener('click', encryptData);
            decryptBtn.addEventListener('click', decryptData);
            clearBtn.addEventListener('click', clearAll);
            copyEncryptedBtn.addEventListener('click', () => copyToClipboard('encrypted-output'));
            copyDecryptedBtn.addEventListener('click', () => copyToClipboard('decrypted-output'));
        });
    </script>
</body>
</html>
