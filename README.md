# 🔗 LinkDetective Scraper

Web-based tool to extract domain and seller data from linkdetective.pro

## 🚀 Quick Deploy to Render.com

1. Fork/Clone this repository
2. Create account on [Render.com](https://render.com)
3. New Web Service → Connect this repository
4. Render will auto-detect configuration
5. Deploy!

Your app will be live at: `https://your-app-name.onrender.com`

## 📋 Files Structure

```
.
├── streamlit_app.py      # Main application
├── requirements.txt      # Python dependencies
├── aptfile              # System packages (chromium)
├── render.yaml          # Render.com configuration
└── README.md            # This file
```

## 🛠️ Local Development

```bash
# Install dependencies
pip install -r requirements.txt

# Run locally
streamlit run streamlit_app.py
```

## 📊 Features

- ✅ Extract domain and seller data
- ✅ Real-time progress tracking
- ✅ Data visualization
- ✅ CSV export
- ✅ Cloud-based (no installation)

## 💡 Usage

1. Open the deployed app
2. Paste your LinkDetective URL (with hash)
3. Click "Start Scraping"
4. Wait for completion
5. Download CSV file

## 🔧 Configuration

### Environment Variables (Optional)

- `PYTHON_VERSION`: 3.11.7 (default)

### Plans

- **Free**: Works but may spin down after inactivity
- **Starter ($7/mo)**: Always on, faster

## 📝 Output Format

CSV file with columns:
- `domain`: Domain name
- `seller`: Seller name
- `price`: Price

## 🐛 Troubleshooting

### Build fails
- Check `requirements.txt` exists
- Verify `aptfile` has correct packages
- Check `render.yaml` syntax

### App doesn't start
- Check logs in Render dashboard
- Verify `streamlit_app.py` has no syntax errors

### Scraping fails
- Verify LinkDetective URL is valid
- Check if hash is expired
- Ensure page structure hasn't changed

## 📄 License

For internal use only.

## 🤝 Support

Issues? Check:
- [Render Documentation](https://render.com/docs)
- [Streamlit Documentation](https://docs.streamlit.io/)

---

**Made with ❤️ using Streamlit & Selenium**
