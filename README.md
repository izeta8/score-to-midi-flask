# 🎼 Score-to-MIDI (Backend)

This is the **backend** for the Score-to-MIDI project. It receives sheet music images from the frontend, processes them using **Audiveris** to extract the music notation, converts the result into a MIDI file using **Music21**, and returns the generated MIDI file.

## 🛠 Technologies Used

- **Audiveris** – Optical Music Recognition (OMR) software for reading sheet music.
- **Music21** – Python library for musical score analysis and conversion.

## 📦 Installation & Setup

### Prerequisites

Ensure you have:

- [Python 3.12.3+](https://www.python.org/)
- [pip](https://pip.pypa.io/en/stable/)

### Installation

1️⃣ Clone the repository and install dependencies:

```bash
git clone https://github.com/spewite/score-to-midi-flask
cd score-to-midi-flask
```

2️⃣ Create a virtual environment and activate it

# On macOS and Linux
```bash
python3 -m venv venv
source venv/bin/activate
```

# On Windows
```bash
python -m venv venv
venv\Scripts\activate
```

3️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

### Run the server

```bash
flask --app app.py --debug run
```

## Environment Variables
```bash
# Configuración del backend
NEXT_PUBLIC_BACKEND_URL=http://127.0.0.1:5000

# URL de la app (se usa para que se rediriga a la misma aplicación despues del pago de Stripe)
NEXT_PUBLIC_APP_URL=http://localhost:3000 


# Secret para la ruta del cron job de la cancelación de suscripción
CRON_SECRET=8f9d7c2e-4c61-4b8e-9c3f-4f2b1a9e7f5d

# Supabase
NEXT_PUBLIC_SUPABASE_URL=https://xjxrgxbphxibtpagzyzj.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InhqeHJneGJwaHhpYnRwYWd6eXpqIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NDgxMDAwMzksImV4cCI6MjA2MzY3NjAzOX0.-s1s1GflJ5IyyBXPUTsJjGRvay-lD5OaKIfob02gccI
SUPABASE_SERVICE_ROLE_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InhqeHJneGJwaHhpYnRwYWd6eXpqIiwicm9sZSI6InNlcnZpY2Vfcm9sZSIsImlhdCI6MTc0ODEwMDAzOSwiZXhwIjoyMDYzNjc2MDM5fQ.rcqvOF2FBahgQOt7PAqNwMmPVByVGGAUSrsSVtxfOqg # Solo para backend

# Configuración de Stripe
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_test_51RS1zSRV7Dh3mrWwfstTxoBXF3K850BZkxPlGmWstrSfB97to7AhD4CtNTehTsNXSlKb2cuECapLQk7eAxnVM2Vt00Z6ZXr1yE
STRIPE_SECRET_KEY=sk_test_51RS1zSRV7Dh3mrWwU15TdpsfRbn1aP3aXw9hyYutt5fryYcvjWootFzR4Ig1PCFBeg6vzD1EVKLmbadqVgZw2vjj00vS9iCb1v
STRIPE_WEBHOOK_SECRET=whsec_c9cda99b6a3cb4a1e660e56a2ce03060d2dff6e6fcd982cfc2e0b3fab4057a1c

# IDs de Precios de Stripe
STRIPE_SUBSCRIPTION_PRICE_ID=price_1RSKd2RV7Dh3mrWwb6AohG0i
STRIPE_ONETIME_MIDI_PRICE_ID=price_1RSKecRV7Dh3mrWwmChGummF

```

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/X8X11EXQLW)

