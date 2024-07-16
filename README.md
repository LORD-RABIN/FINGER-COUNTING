<h1>FINGER COUNTING CODE</h1>
<h3>INSTALLATION </h3>
<style>
    .container {
        width: 300px;
        margin: 20px auto;
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 5px;
        background-color: #f9f9f9;
    }
    .copy-button {
        margin-top: 10px;
        padding: 5px 10px;
        background-color: #4CAF50;
        border: none;
        color: white;
        border-radius: 3px;
        cursor: pointer;
    }
</style>
</head>
<body>

<div class="container">
    <textarea id="copyTextarea" rows="4" readonly>This is the text to copy.</textarea>
    <button class="copy-button" onclick="copyToClipboard()">Copy Text</button>
</div>

<script>
function copyToClipboard() {
    var copyText = document.getElementById("copyTextarea");
    
    // Select the text inside the textarea
    copyText.select();
    copyText.setSelectionRange(0, 99999); // For mobile devices
    
    // Copy the selected text to the clipboard
    document.execCommand("copy");
    
    // Deselect the textarea
    copyText.setSelectionRange(0, 0);
    
    // Change button text to indicate copied
    var button = document.querySelector('.copy-button');
    button.textContent = 'Copied!';
    setTimeout(function() {
        button.textContent = 'Copy Text';
    }, 1500);
}
</script>
