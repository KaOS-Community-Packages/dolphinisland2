pkgname=dolphinisland2
pkgver=1.0
pkgrel=1
pkgdesc="Dolphin Island 2 is a game made by Jan (@AldianSolkai) and James (@jtangc) for the A Game By It's Cover 2015 Game Jam."
arch=('x86_64')
url="https://aldiansolkai.itch.io/dolphin-island-2"
license=('MIT')
depends=('godot')
source=("https://github.com/janmarcano/Dolphin-Island-2/archive/master.zip"
        'dolphinisland2.desktop'
        'launch-dolphinisland2.sh')
md5sums=('35a29e99661d7513de6b9f0f9d19afaa'
         '697afab91d96980598b31349f530b966'
         '743f962456573f9b67c1d9604521081c')

package() {
    cd Dolphin-Island-2-master
    
    install -d ${pkgdir}/opt/dolphinisland2
    cp -r * ${pkgdir}/opt/dolphinisland2/
    chmod 755 -R ${pkgdir}/opt/dolphinisland2
    
    install -Dm755 ${srcdir}/launch-dolphinisland2.sh ${pkgdir}/usr/bin/launch-dolphinisland2.sh
    install -Dm644 $srcdir/dolphinisland2.desktop ${pkgdir}/usr/share/applications/dolphinisland2.desktop
    install -Dm644 ${srcdir}/Dolphin-Island-2-master/icon.png ${pkgdir}/usr/share/pixmaps/dolphinisland2.png
}
