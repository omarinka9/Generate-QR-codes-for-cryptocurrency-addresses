# Generate-QR-codes-for-cryptocurrency-addresses
Generate QR codes for cryptocurrency addresses

import qrcode
import os

def generate_qr_code(address):
    img = qrcode.make(address)
    filename = f'{address[:8]}_qr.png'
    img.save(filename)
    print(f'QR-код сохранен как {filename}')

if __name__ == '__main__':
    address = 'bc1qxxxxxxxyyzzzzzzz'  # Ваш криптовалютный адрес
    generate_qr_code(address)
