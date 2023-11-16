import hashlib


def sha256_hash(data):
    # Convert data to bytes if it's not already in bytes
    if not isinstance(data, bytes):
        data = str(data).encode('utf-8')  # Assuming UTF-8 encoding, change if needed

    # Generate SHA-256 hash
    hashed = hashlib.sha256(data).hexdigest()
    return hashed


# Example usage:
text_to_hash =input( "Enter the text to convert into hash")
hashed_text = sha256_hash(text_to_hash)
print("SHA-256 hash:", hashed_text)
