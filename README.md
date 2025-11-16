<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>One-Click Copy</title>
<style>
  body { font-family: sans-serif; max-width: 700px; margin: 40px auto; }
  textarea { width: 100%; height: 300px; padding: 10px; font-size: 16px; }
  button { margin-top: 15px; padding: 10px 16px; font-size: 16px; cursor: pointer; }
</style>
</head>
<body>

<h2>Your Text</h2>

<textarea id="textContent">
Paste or edit your long text here before deploying... 
</textarea>

<button onclick="copyText()">Copy All Text</button>

<script>
function copyText() {
  const text = document.getElementById('textContent').value;
  navigator.clipboard.writeText(text)
    .then(() => alert("Copied!"))
    .catch(err => alert("Copy failed: " + err));
}
</script>

</body>
</html>
