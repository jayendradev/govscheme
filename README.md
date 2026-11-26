# Govt. Schemes / सरकारी योजनाएँ

हिंदी वेबसाइट: केंद्र और राज्य की सरकारी योजनाएँ, पात्रता और उनका लाभ कैसे लें।

तकनीक TheBriefWire जैसी है: Next.js, React, TypeScript, Bootstrap, और Django REST Framework।

यह साइट किसी मंत्रालय की आधिकारिक वेबसाइट नहीं है। हर पृष्ठ आधिकारिक पोर्टल की ओर लिंक करता है। राशि और तिथि वहीं जाँचें।

## साइट चलाएँ

```bash
cd frontend
npm install
npm run dev
```

मुखपृष्ठ: http://localhost:3010

## Django एपीआई (वैकल्पिक)

सामग्री का स्रोत `frontend/src/data/catalog.json` है। Django वही फ़ाइल पढ़कर एडमिन और एपीआई भरता है।

```bash
cd backend
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py seed_catalog
python manage.py createsuperuser
python manage.py runserver 127.0.0.1:8000
```

एडमिन: http://127.0.0.1:8000/admin/

एपीआई से पढ़ने के लिए `frontend/.env.local` में लिखें:

```
YOJANA_API_URL=http://127.0.0.1:8000
```

बिना इस चर के साइट कैटलॉग फ़ाइल से ही बनती है।
# govscheme
