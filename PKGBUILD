pkgname=pipewire-s6
pkgver=0.1.0
pkgrel=1
pkgdesc='Per-user s6 service definitions for PipeWire, PipeWire Pulse, and WirePlumber'
arch=('any')
url='https://github.com/username13121/pipewire-s6-artix'
license=('0BSD')
depends=('pipewire' 'pipewire-pulse' 'wireplumber')
provides=('pipewire-pulse-s6' 'wireplumber-s6')
conflicts=('pipewire-s6-user' 'pipewire-pulse-s6-user' 'wireplumber-s6-user'
           'pipewire-pulse-s6' 'wireplumber-s6')
replaces=('pipewire-s6-user' 'pipewire-pulse-s6-user' 'wireplumber-s6-user'
          'pipewire-pulse-s6' 'wireplumber-s6')
source=('pw-type'
        'pw-run'
        'pw-notification-fd'
        'pw-timeout-up'
        'pw-flag-recommended'
        'pw-check'
        'pulse-type'
        'pulse-run'
        'pulse-notification-fd'
        'pulse-timeout-up'
        'pulse-flag-recommended'
        'pulse-dependency-pipewire'
        'pulse-check'
        'wireplumber-type'
        'wireplumber-run'
        'wireplumber-flag-recommended'
        'wireplumber-dependency-pipewire'
        'LICENSE')
sha256sums=('d0001a150b83f68f09004c5059045cb76a3f064eed4d42ce072bc3722c118006'
            '4d1fd1951cc45b6faab1400e657243ef22c9502dee4f0e8e220c93d05e45834f'
            '1121cfccd5913f0a63fec40a6ffd44ea64f9dc135c66634ba001d10bcf4302a2'
            '876e13f4e07bb39705302c01f445ffd2d2c3b180a207e4d959d6b671c67da09b'
            'e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855'
            '7d1c090cf1ecbfc8a61dd1389dd219c74750682ef83b7e767b42aaaf45f3c72e'
            'd0001a150b83f68f09004c5059045cb76a3f064eed4d42ce072bc3722c118006'
            '00ca70c406bcb904c2ca3e3de48bbd31fbb8b3f37dca9f9cb1138c5665de773e'
            '1121cfccd5913f0a63fec40a6ffd44ea64f9dc135c66634ba001d10bcf4302a2'
            '876e13f4e07bb39705302c01f445ffd2d2c3b180a207e4d959d6b671c67da09b'
            'e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855'
            'e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855'
            'ab40eef9625493db0c4a55cc4acd81ebd8f45f15c3e1ed66f60b046d0a993e87'
            'd0001a150b83f68f09004c5059045cb76a3f064eed4d42ce072bc3722c118006'
            '5adb4d61a5fd7ef7992ed92b048ac1933fe646415f6d64c09c53708a5bfd9326'
            'e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855'
            'e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855'
            'e43689ed5dbd460be77c4f8ecc14a1285671194f11f711520a7be8d8d6d847f7')

package() {
    local store="$pkgdir/etc/s6/user/sv"
    local dest

    dest="$store/pipewire"
    install -Dm644 pw-type "$dest/type"
    install -Dm755 pw-run "$dest/run"
    install -Dm644 pw-notification-fd "$dest/notification-fd"
    install -Dm644 pw-timeout-up "$dest/timeout-up"
    install -Dm644 pw-flag-recommended "$dest/flag-recommended"
    install -Dm755 pw-check "$dest/data/check"

    dest="$store/pipewire-pulse"
    install -Dm644 pulse-type "$dest/type"
    install -Dm755 pulse-run "$dest/run"
    install -Dm644 pulse-notification-fd "$dest/notification-fd"
    install -Dm644 pulse-timeout-up "$dest/timeout-up"
    install -Dm644 pulse-flag-recommended "$dest/flag-recommended"
    install -Dm644 pulse-dependency-pipewire "$dest/dependencies.d/pipewire"
    install -Dm755 pulse-check "$dest/data/check"

    dest="$store/wireplumber"
    install -Dm644 wireplumber-type "$dest/type"
    install -Dm755 wireplumber-run "$dest/run"
    install -Dm644 wireplumber-flag-recommended "$dest/flag-recommended"
    install -Dm644 wireplumber-dependency-pipewire "$dest/dependencies.d/pipewire"

    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
