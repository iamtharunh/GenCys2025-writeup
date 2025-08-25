this was a very tough challenge 

key is abc12

and we have random 15 number

i used chatgpt

it decoded and said USTCt']Tflag}

i tried abc12abc12 it gave the same

chatgpt said to try abc12xyz12 i got somethinng like USTCtf{DlTflag}

all are plaintext

i asked to give bruteforce code it gave a code

```py
# brute_force_xor_key.py

ciphertext = [52, 49, 55, 114, 70, 30, 2, 62, 93, 102, 7, 14, 2, 86, 79]

# Base key prefix
base_key = b'abc12xyz'  # first 8 bytes fixed

# Function to XOR decrypt with repeating key
def xor_decrypt(data, key):
    return ''.join(
        chr(byte ^ key[i % len(key)]) for i, byte in enumerate(data)
    )

# Brute-force last two digits from '12' to '99'
for i in range(12, 100):
    # Format last two digits as string and encode to bytes
    last_two = f"{i:02}".encode()
    key = base_key + last_two
    plaintext = xor_decrypt(ciphertext, key)
    print(f"Key: {key} -> Decrypted: {plaintext}")

i got a huge output
Key: b'abc12xyz12' -> Decrypted: USTCtf{DlTflag}
Key: b'abc12xyz13' -> Decrypted: USTCtf{DlUflag}
Key: b'abc12xyz14' -> Decrypted: USTCtf{DlRflag}
Key: b'abc12xyz15' -> Decrypted: USTCtf{DlSflag}
Key: b'abc12xyz16' -> Decrypted: USTCtf{DlPflag}
Key: b'abc12xyz17' -> Decrypted: USTCtf{DlQflag}
Key: b'abc12xyz18' -> Decrypted: USTCtf{Dl^flag}
Key: b'abc12xyz19' -> Decrypted: USTCtf{Dl_flag}
Key: b'abc12xyz20' -> Decrypted: USTCtf{DoVflag}
Key: b'abc12xyz21' -> Decrypted: USTCtf{DoWflag}
Key: b'abc12xyz22' -> Decrypted: USTCtf{DoTflag}
Key: b'abc12xyz23' -> Decrypted: USTCtf{DoUflag}
Key: b'abc12xyz24' -> Decrypted: USTCtf{DoRflag}
Key: b'abc12xyz25' -> Decrypted: USTCtf{DoSflag}
Key: b'abc12xyz26' -> Decrypted: USTCtf{DoPflag}
Key: b'abc12xyz27' -> Decrypted: USTCtf{DoQflag}
Key: b'abc12xyz28' -> Decrypted: USTCtf{Do^flag}
Key: b'abc12xyz29' -> Decrypted: USTCtf{Do_flag}
Key: b'abc12xyz30' -> Decrypted: USTCtf{DnVflag}
Key: b'abc12xyz31' -> Decrypted: USTCtf{DnWflag}
Key: b'abc12xyz32' -> Decrypted: USTCtf{DnTflag}
Key: b'abc12xyz33' -> Decrypted: USTCtf{DnUflag}
Key: b'abc12xyz34' -> Decrypted: USTCtf{DnRflag}
Key: b'abc12xyz35' -> Decrypted: USTCtf{DnSflag}
Key: b'abc12xyz36' -> Decrypted: USTCtf{DnPflag}
Key: b'abc12xyz37' -> Decrypted: USTCtf{DnQflag}
Key: b'abc12xyz38' -> Decrypted: USTCtf{Dn^flag}
Key: b'abc12xyz39' -> Decrypted: USTCtf{Dn_flag}
Key: b'abc12xyz40' -> Decrypted: USTCtf{DiVflag}
Key: b'abc12xyz41' -> Decrypted: USTCtf{DiWflag}
Key: b'abc12xyz42' -> Decrypted: USTCtf{DiTflag}
Key: b'abc12xyz43' -> Decrypted: USTCtf{DiUflag}
Key: b'abc12xyz44' -> Decrypted: USTCtf{DiRflag}
Key: b'abc12xyz45' -> Decrypted: USTCtf{DiSflag}
Key: b'abc12xyz46' -> Decrypted: USTCtf{DiPflag}
Key: b'abc12xyz47' -> Decrypted: USTCtf{DiQflag}
Key: b'abc12xyz48' -> Decrypted: USTCtf{Di^flag}
Key: b'abc12xyz49' -> Decrypted: USTCtf{Di_flag}
Key: b'abc12xyz50' -> Decrypted: USTCtf{DhVflag}
Key: b'abc12xyz51' -> Decrypted: USTCtf{DhWflag}
Key: b'abc12xyz52' -> Decrypted: USTCtf{DhTflag}
Key: b'abc12xyz53' -> Decrypted: USTCtf{DhUflag}
Key: b'abc12xyz54' -> Decrypted: USTCtf{DhRflag}
Key: b'abc12xyz55' -> Decrypted: USTCtf{DhSflag}
Key: b'abc12xyz56' -> Decrypted: USTCtf{DhPflag}
Key: b'abc12xyz57' -> Decrypted: USTCtf{DhQflag}
Key: b'abc12xyz58' -> Decrypted: USTCtf{Dh^flag}
Key: b'abc12xyz59' -> Decrypted: USTCtf{Dh_flag}
Key: b'abc12xyz60' -> Decrypted: USTCtf{DkVflag}
Key: b'abc12xyz61' -> Decrypted: USTCtf{DkWflag}
Key: b'abc12xyz62' -> Decrypted: USTCtf{DkTflag}
Key: b'abc12xyz63' -> Decrypted: USTCtf{DkUflag}
Key: b'abc12xyz64' -> Decrypted: USTCtf{DkRflag}
Key: b'abc12xyz65' -> Decrypted: USTCtf{DkSflag}
Key: b'abc12xyz66' -> Decrypted: USTCtf{DkPflag}
Key: b'abc12xyz67' -> Decrypted: USTCtf{DkQflag}
Key: b'abc12xyz68' -> Decrypted: USTCtf{Dk^flag}
Key: b'abc12xyz69' -> Decrypted: USTCtf{Dk_flag}
Key: b'abc12xyz70' -> Decrypted: USTCtf{DjVflag}
Key: b'abc12xyz71' -> Decrypted: USTCtf{DjWflag}
Key: b'abc12xyz72' -> Decrypted: USTCtf{DjTflag}
Key: b'abc12xyz73' -> Decrypted: USTCtf{DjUflag}
Key: b'abc12xyz74' -> Decrypted: USTCtf{DjRflag}
Key: b'abc12xyz75' -> Decrypted: USTCtf{DjSflag}
Key: b'abc12xyz76' -> Decrypted: USTCtf{DjPflag}
Key: b'abc12xyz77' -> Decrypted: USTCtf{DjQflag}
Key: b'abc12xyz78' -> Decrypted: USTCtf{Dj^flag}
Key: b'abc12xyz79' -> Decrypted: USTCtf{Dj_flag}
Key: b'abc12xyz80' -> Decrypted: USTCtf{DeVflag}
Key: b'abc12xyz81' -> Decrypted: USTCtf{DeWflag}
Key: b'abc12xyz82' -> Decrypted: USTCtf{DeTflag}
Key: b'abc12xyz83' -> Decrypted: USTCtf{DeUflag}
Key: b'abc12xyz84' -> Decrypted: USTCtf{DeRflag}
Key: b'abc12xyz85' -> Decrypted: USTCtf{DeSflag}
Key: b'abc12xyz86' -> Decrypted: USTCtf{DePflag}
Key: b'abc12xyz87' -> Decrypted: USTCtf{DeQflag}
Key: b'abc12xyz88' -> Decrypted: USTCtf{De^flag}
Key: b'abc12xyz89' -> Decrypted: USTCtf{De_flag}
Key: b'abc12xyz90' -> Decrypted: USTCtf{DdVflag}
Key: b'abc12xyz91' -> Decrypted: USTCtf{DdWflag}
Key: b'abc12xyz92' -> Decrypted: USTCtf{DdTflag}
Key: b'abc12xyz93' -> Decrypted: USTCtf{DdUflag}
Key: b'abc12xyz94' -> Decrypted: USTCtf{DdRflag}
Key: b'abc12xyz95' -> Decrypted: USTCtf{DdSflag}
Key: b'abc12xyz96' -> Decrypted: USTCtf{DdPflag}
Key: b'abc12xyz97' -> Decrypted: USTCtf{DdQflag}
Key: b'abc12xyz98' -> Decrypted: USTCtf{Dd^flag}
Key: b'abc12xyz99' -> Decrypted: USTCtf{Dd_flag}
```

i randomly tried to put the flag, it didnt work, i thought Dj_flag is good(music) but didnt work. then i tried De_flag it worked (idk whats the logic behind randomly got this)


