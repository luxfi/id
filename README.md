# Lux ID

Lux ID is a modern Identity and Access Management (IAM) system based on Casdoor, customized for the Lux Network ecosystem. It provides comprehensive authentication and authorization services with support for OAuth 2.0, OIDC, SAML, CAS, LDAP, SCIM, WebAuthn, TOTP, MFA and RADIUS protocols.

## Features

- 🔐 **Multi-Protocol Support**: OAuth 2.0, OpenID Connect, SAML, CAS, LDAP, RADIUS
- 🛡️ **Advanced Security**: WebAuthn, TOTP, MFA, Passwordless authentication
- 🎨 **Customizable UI**: Modern, responsive interface with Lux branding (black theme)
- 🌐 **Multi-Tenancy**: Support for multiple organizations and applications
- 🔄 **SSO Integration**: Seamless Single Sign-On across Lux services
- 📊 **Comprehensive Admin Panel**: User management, role-based access control, audit logs
- 🚀 **High Performance**: Built with Go for speed and reliability
- 🐳 **Cloud Native**: Docker-ready with Kubernetes support

## Quick Start

### Using Docker Compose

```bash
# Clone the repository
git clone https://github.com/luxdefi/id.git lux-id
cd lux-id

# Start services
docker compose up -d

# Access Lux ID at http://localhost:8000
```

### Development Setup

```bash
# Backend
go mod download
go run main.go

# Frontend (in another terminal)
cd web
yarn install
yarn start
```

## Configuration

Edit `conf/app.conf` to configure:

- Database connection (MySQL/PostgreSQL)
- Redis connection
- OAuth providers
- SMTP settings
- And more...

## Environment Variables

- `MYSQL_ROOT_PASSWORD`: Database root password
- `REDIS_PASSWORD`: Redis password (if enabled)
- `LUX_ID_SECRET`: Application secret key

## Default Credentials

- Username: `admin`
- Password: `123456`

⚠️ **Important**: Change the default password immediately after first login.

## API Documentation

Swagger documentation is available at: `http://localhost:8000/swagger/`

## Deployment

### Production with Traefik

```bash
docker compose -f compose.prod.yaml up -d
```

This will deploy Lux ID with:
- Automatic SSL/TLS via Let's Encrypt
- Traefik reverse proxy
- Production-ready MySQL and Redis
- Available at https://id.lux.network

### Development Environment

```bash
docker compose -f compose.dev.yaml up -d
```

Available at https://id-dev.lux.network

## Integration with Lux Services

Lux ID seamlessly integrates with:

- **Lux Node**: Blockchain validator authentication
- **Lux Wallet**: Secure wallet access
- **Lux Bridge**: Cross-chain identity verification
- **Lux Exchange**: Trading platform authentication

## Branding Customization

Lux ID features a sleek black theme optimized for the Lux Network brand. The UI is easily customizable:

- Logo files in `/web/public/logo/`
- Theme configuration in `/web/src/theme/`
- Color scheme uses black background with gold accents (#FFD700)

To update branding:
1. Replace logo files in `/web/public/logo/`
2. Update theme colors in `/web/src/theme/index.js`
3. Rebuild frontend: `cd web && yarn build`

## Security

- All passwords are hashed using Argon2id
- Support for hardware security keys (WebAuthn)
- Built-in rate limiting and brute force protection
- Comprehensive audit logging
- CSRF protection
- XSS prevention

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

## License

Lux ID is licensed under the Apache License 2.0. See [LICENSE](LICENSE) for details.

## Support

- Documentation: https://docs.lux.network/id
- Issues: https://github.com/luxdefi/id/issues
- Discord: https://discord.gg/luxnetwork

## Acknowledgments

Lux ID is based on the excellent [Casdoor](https://github.com/casdoor/casdoor) project. We're grateful to the Casdoor team for creating such a robust IAM foundation.

---

Built with ⚡ by the Lux Network team