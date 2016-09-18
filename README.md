**Instant.io Snap**

*Notes*

 * A nodejs app which uses webtorrent.
 * I made a fork of the nodejs plugin so I could add a build step which does `npm run build`, because without this the app will try and do that on first launch, which fails in a readonly snap.

*Building*

On an up-to-date 16.04 system, install snapcraft and run `snapcraft` in the same directory as this README

*Things which work*

* The initial `npm install` from the plugin works

*Things which don't work*

 * The extra step I added to the nodejs plugin doesn't work. It fails to `cd` to the installdir where the `npm run build` step should run. Output at this [paste](http://paste.ubuntu.com/23196865/)
