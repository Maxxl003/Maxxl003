# Der verschlüsselte Text
verschluesselter_text = "Fw gjvu jvs jpwqi Xf xlih"  # Verschlüsselt mit Caesar-Chiffre (Shift 4)

# Funktion zur Entschlüsselung
def entschluesseln(text, shift):
    entschluesselter_text = ""
    for char in text:
        if char.isalpha():  # Nur Buchstaben verschlüsseln
            shifted = chr((ord(char) - shift - 65) % 26 + 65) if char.isupper() else chr((ord(char) - shift - 97) % 26 + 97)
            entschluesselter_text += shifted
        else:
            entschluesselter_text += char  # Nicht-Buchstaben bleiben gleich
    return entschluesselter_text

# Brute-Force-Entschlüsselung
def brute_force_entschluesseln(text):
    for shift in range(1, 26):  # Alle möglichen Verschiebungen ausprobieren
        print(f"Shift {shift}: {entschluesseln(text, shift)}")

# Programm ausführen
brute_force_entschluesseln(verschluesselter_text)
<!---
Maxxl003/Maxxl003 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
