import phonenumbers
from phonenumbers import carrier, geocoder, timezone

def track_phone_number():
    nomor = input("Masukkan nomor telepon ( +6282241900058): ")
    try:
        parsed_number = phonenumbers.parse(nomor, "ID")  # "ID" untuk Indonesia
    except phonenumbers.NumberParseException:
        print("Nomor telepon tidak valid.")
        return
