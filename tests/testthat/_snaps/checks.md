# check_wcs_version() works

    Code
      emdn_init_wcs_client("human_activities", "1.1.0")
    Condition
      Warning:
      ! Service version "1.1.0" can result in unexpected behaviour on the "human activities" server. We strongly recommend reconnecting using `service_version` "2.0.1".
    Output
      <WCSClient>
      ....|-- url: https://ows.emodnet-humanactivities.eu/wcs
      ....|-- version: 1.1.0
      ....|-- capabilities <WCSCapabilities>

---

    Code
      emdn_init_wcs_client("biology", "2.1.0")
    Condition
      Warning:
      ! Service version "2.1.0" not supported by server and can result in unexpected behaviour.
      We strongly recommend reconnecting using one of the supported versions:
      "2.0.1", "1.1.1", and "1.1.0"
    Output
      <WCSClient>
      ....|-- url: https://geo.vliz.be/geoserver/Emodnetbio/wcs
      ....|-- version: 2.1.0
      ....|-- capabilities <WCSCapabilities>

