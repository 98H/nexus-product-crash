# Deployment & Operations Guide: Product Crash

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-product-crash-47ef84/](/preview/prod-product-crash-47ef84/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-19T21:12:42.833892+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=Product Crash Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/pytest-of-root/pytest-0/test_exception_containment_in_0/workspaces/prod-product-crash-47ef84
ExecStart=/usr/bin/python3 /tmp/pytest-of-root/pytest-0/test_exception_containment_in_0/workspaces/prod-product-crash-47ef84/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.
