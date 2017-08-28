---
layout: post
title:  "The journey..."
excerpt: "With the end of GSoC coding period only a couple of days away, lets have a look at what I've been able to accomplish so far."
---

With the end of GSoC coding period only a couple of days away, lets have a look at what I've been able to accomplish so far.
My project, as I initially told, was divided into three main parts.

* Removing nose as a dependency
  * `nose` is no longer required for the TravisCI build to pass. We have completely shifted to `pytest`.

* Improving performance and bringing down the execution time taken by the TravisCI build.
  * Have brought down the execution time significantly. The TravisCI build that used to take ~45-50 mins(and sometimes timeout due to the 50min time limit)
  now completes in ~20 minutes! We no longer have to restart builds and _hope_ they complete.
  * Have completely ported 7 out of 8 modules in `MDAnalysisTests` to follow the `pytest` style. The `coordinates` module is still work-in-progress and
  needs some more refining. I am working on it as of now and hope to complete it in a week.

* Refactoring format specific reader/writer classes to make them follow the same base API (Optional).
  * Unfortunately, I couldn't make time to take this on. Thanks to the community for pointing out, during the application phase, that I might not be able to
  get here!

Let's have a look at some numbers. I've opened a total of 112 PRs and have got 128 commits merged as of today. Lines of code is an interesting story - I've managed to delete more lines than I've added! _Less code == Less maintenance effort._

In the end, GSoC has been a great experience. I've picked up a couple of things about programming and testing while working with the community and this has certainly helped me grow as a developer. My project wouldn't have been possible without all the valuable help I got along the way. A huge, huge thanks to my mentors and the whole community for all the help, ideas and discussions along the way.

So what's next? First of all, I'll complete my work on the `coordinates` module. Once that's done, I plan to take on Part 3 of my proposal - Refactoring format specific reader/writer classes to make them follow the same base API. Though I won't be able to dedicate as much time as I've been doing during the GSoC coding period, I'll try to keep working on this regularly.

Finally here's a list of all the PRs that I worked on during the summer -

* [#1370](https://github.com/MDAnalysis/mdanalysis/pull/1370) Break build packagewise
* [#1413](https://github.com/MDAnalysis/mdanalysis/pull/1413) Port lib/test_util.py to pytest
* [#1414](https://github.com/MDAnalysis/mdanalysis/pull/1414) Port coordinates module
* [#1417](https://github.com/MDAnalysis/mdanalysis/pull/1417) Port formats module to pytest
* [#1418](https://github.com/MDAnalysis/mdanalysis/pull/1418) Run the pytest testsuite in parallel
* [#1420](https://github.com/MDAnalysis/mdanalysis/pull/1420) Port topology module
* [#1434](https://github.com/MDAnalysis/mdanalysis/pull/1434) Port utils module to pytest
* [#1439](https://github.com/MDAnalysis/mdanalysis/pull/1439) Port auxiliary module to pytest
* [#1441](https://github.com/MDAnalysis/mdanalysis/pull/1441) Fix coverage drop in coordinates module
* [#1443](https://github.com/MDAnalysis/mdanalysis/pull/1443) Port core module to pytest
* [#1450](https://github.com/MDAnalysis/mdanalysis/pull/1450) Port analysis module to pytes
* [#1464](https://github.com/MDAnalysis/mdanalysis/pull/1464) Pytest Style: test_altloc.py
* [#1465](https://github.com/MDAnalysis/mdanalysis/pull/1465) Pytest style: test_datafiles.py
* [#1466](https://github.com/MDAnalysis/mdanalysis/pull/1466) Pytest Style: test_deprecated.py
* [#1467](https://github.com/MDAnalysis/mdanalysis/pull/1467) Pytest Style: test_log.py
* [#1468](https://github.com/MDAnalysis/mdanalysis/pull/1468) Pytest Style: test_modelling.py
* [#1469](https://github.com/MDAnalysis/mdanalysis/pull/1469) Pytest Style: test_nuclinfo.py
* [#1470](https://github.com/MDAnalysis/mdanalysis/pull/1470) Pytest Style: test_persistence.py
* [#1471](https://github.com/MDAnalysis/mdanalysis/pull/1471) Pytest Style: test_selections.py
* [#1472](https://github.com/MDAnalysis/mdanalysis/pull/1472) Pytest Style: test_streamio.py
* [#1473](https://github.com/MDAnalysis/mdanalysis/pull/1473) Pytest Style: test_imports.py
* [#1480](https://github.com/MDAnalysis/mdanalysis/pull/1480) Dropping nose as a dependency
* [#1492](https://github.com/MDAnalysis/mdanalysis/pull/1492) Pytest Style: auxiliary/base.py
* [#1493](https://github.com/MDAnalysis/mdanalysis/pull/1493) Pytest Style: test_xvg.py
* [#1494](https://github.com/MDAnalysis/mdanalysis/pull/1494) Pytest Style: test_util.py
* [#1526](https://github.com/MDAnalysis/mdanalysis/pull/1526) Pytest Style: topology/base.py
* [#1527](https://github.com/MDAnalysis/mdanalysis/pull/1527) Pytest Style: topology/test_crd.py
* [#1535](https://github.com/MDAnalysis/mdanalysis/pull/1535) Pytest Style: core/test_atom.py
* [#1539](https://github.com/MDAnalysis/mdanalysis/pull/1539) Pytest Style analysis/test_hole.py
* [#1540](https://github.com/MDAnalysis/mdanalysis/pull/1540) Pytest Style analysis/test_diffusionmap.py
* [#1541](https://github.com/MDAnalysis/mdanalysis/pull/1541) Pytest style analysis/test_distances.py
* [#1542](https://github.com/MDAnalysis/mdanalysis/pull/1542) Pytest Style analysis/test_gnm.py
* [#1543](https://github.com/MDAnalysis/mdanalysis/pull/1543) Pytest Style analysis/test_density.py
* [#1544](https://github.com/MDAnalysis/mdanalysis/pull/1544) Pytest Style analysis/test_hbonds.py
* [#1545](https://github.com/MDAnalysis/mdanalysis/pull/1545) Pytest Style analysis/test_contacts.py
* [#1546](https://github.com/MDAnalysis/mdanalysis/pull/1546) Pytest Style analysis/test_align.py
* [#1547](https://github.com/MDAnalysis/mdanalysis/pull/1547) Pytest Style analysis/test_base.py
* [#1548](https://github.com/MDAnalysis/mdanalysis/pull/1548) Pytest Style analysis/test_lineardensity.py
* [#1549](https://github.com/MDAnalysis/mdanalysis/pull/1549) Pytest Style analysis/test_nuclinfo.py
* [#1550](https://github.com/MDAnalysis/mdanalysis/pull/1550) Pytest Style analysis/test_helanal.py
* [#1551](https://github.com/MDAnalysis/mdanalysis/pull/1551) Pytest Style analysis/test_leaflet.py
* [#1568](https://github.com/MDAnalysis/mdanalysis/pull/1568) Pytest style analysis/test_persistencelength.py
* [#1569](https://github.com/MDAnalysis/mdanalysis/pull/1569) Pytest Style analysis/test_psa.py
* [#1570](https://github.com/MDAnalysis/mdanalysis/pull/1570) Pytest Style analysis/test_rdf.py
* [#1571](https://github.com/MDAnalysis/mdanalysis/pull/1571) Pytest Style analysis/test_waterdynamics.py
* [#1574](https://github.com/MDAnalysis/mdanalysis/pull/1574) Remove dependency from nose
* [#1586](https://github.com/MDAnalysis/mdanalysis/pull/1586) Pytest Style topology/test_dlpoly.py
* [#1587](https://github.com/MDAnalysis/mdanalysis/pull/1587) Pytest Style topology/test_dms.py
* [#1588](https://github.com/MDAnalysis/mdanalysis/pull/1588) Pytest Style topology/test_gms.py
* [#1590](https://github.com/MDAnalysis/mdanalysis/pull/1590) Pytest Style topology/test_gro.py
* [#1592](https://github.com/MDAnalysis/mdanalysis/pull/1592) Pytest Style topology/test_guessers.py
* [#1593](https://github.com/MDAnalysis/mdanalysis/pull/1593) Pytest Style topology/test_hoomdxml.py
* [#1595](https://github.com/MDAnalysis/mdanalysis/pull/1595) Pytest Style topology/test_mmtf.py
* [#1596](https://github.com/MDAnalysis/mdanalysis/pull/1596) Pytest Style topology/test_lammpsdata.py
* [#1597](https://github.com/MDAnalysis/mdanalysis/pull/1597) Pytest Style topology/test_mol2.py
* [#1598](https://github.com/MDAnalysis/mdanalysis/pull/1598) Pytest Style topology/test_pdb.py
* [#1599](https://github.com/MDAnalysis/mdanalysis/pull/1599) Pytest Style topology/test_pdbqt.py
* [#1600](https://github.com/MDAnalysis/mdanalysis/pull/1600) Pytest Style topology/test_pqr.py
* [#1601](https://github.com/MDAnalysis/mdanalysis/pull/1601) Pytest Style topology/test_psf.py
* [#1602](https://github.com/MDAnalysis/mdanalysis/pull/1602) Pytest Style topology/test_top.py
* [#1604](https://github.com/MDAnalysis/mdanalysis/pull/1604) Pytest Style topology/test_topology_base.py
* [#1605](https://github.com/MDAnalysis/mdanalysis/pull/1605) PEP8 fixes topology/test_topology_str_types.py
* [#1607](https://github.com/MDAnalysis/mdanalysis/pull/1607) Pytest Style topology/test_xpdb.py
* [#1608](https://github.com/MDAnalysis/mdanalysis/pull/1608) Pytest Style topology/test_xyz.py
* [#1610](https://github.com/MDAnalysis/mdanalysis/pull/1610) Pytest Style analysis/test_rms.py
* [#1611](https://github.com/MDAnalysis/mdanalysis/pull/1611) Pytest Style analysis/test_hydrogenbondautocorrel.py
* [#1620](https://github.com/MDAnalysis/mdanalysis/pull/1620) Pytest Style core/test_topologyattrs.py
* [#1621](https://github.com/MDAnalysis/mdanalysis/pull/1621) Pytest Stylecore/test_topology.py
* [#1622](https://github.com/MDAnalysis/mdanalysis/pull/1622) Pytest Style core/test_segmentgroup.py
* [#1623](https://github.com/MDAnalysis/mdanalysis/pull/1623) Pytest Style core/test_segment.py
* [#1624](https://github.com/MDAnalysis/mdanalysis/pull/1624) Pytest Style core/test_residuegroup.py
* [#1625](https://github.com/MDAnalysis/mdanalysis/pull/1625) Pytest Style core/test_residue.py
* [#1626](https://github.com/MDAnalysis/mdanalysis/pull/1626) Pytest Style core/test_requires.py
* [#1627](https://github.com/MDAnalysis/mdanalysis/pull/1627) Pytest Style core/test_index_dtype.py
* [#1628](https://github.com/MDAnalysis/mdanalysis/pull/1628) Pytest Style core/test_groups.py
* [#1629](https://github.com/MDAnalysis/mdanalysis/pull/1629) Pytest Style core/test_group_traj_access.py
* [#1633](https://github.com/MDAnalysis/mdanalysis/pull/1633) Pytest Style core/test_fragments.py
* [#1634](https://github.com/MDAnalysis/mdanalysis/pull/1634) Pytest Style core/test_atomselections.py
* [#1637](https://github.com/MDAnalysis/mdanalysis/pull/1637) Pytest Style coordinates/test_dlpoly.py
* [#1638](https://github.com/MDAnalysis/mdanalysis/pull/1638) Pytest Style coordinates/test_dms.py
* [#1639](https://github.com/MDAnalysis/mdanalysis/pull/1639) Pytest Style coordinates/test_gms.py
* [#1640](https://github.com/MDAnalysis/mdanalysis/pull/1640) Pytest Style coordinates/test_chainreader.py
* [#1641](https://github.com/MDAnalysis/mdanalysis/pull/1641) Pytest Style coordinates/test_crd.py
* [#1644](https://github.com/MDAnalysis/mdanalysis/pull/1644) Pytest Style coordinates/test_lammps.py
* [#1645](https://github.com/MDAnalysis/mdanalysis/pull/1645) Pytest Style coordinates/test_memory.py
* [#1646](https://github.com/MDAnalysis/mdanalysis/pull/1646) Pytest Style coordinates/test_mmtf.py
* [#1647](https://github.com/MDAnalysis/mdanalysis/pull/1647) Pytest Style coordinates/test_netcdf.py & coordinates/test_trj.py
* [#1648](https://github.com/MDAnalysis/mdanalysis/pull/1648) Pytest Style coordinates/test_null.py
* [#1649](https://github.com/MDAnalysis/mdanalysis/pull/1649) Pytest Style coordinates/test_pdbqt.py
* [#1650](https://github.com/MDAnalysis/mdanalysis/pull/1650) Pytest Style coordinates/test_timestep_api.py
* [#1652](https://github.com/MDAnalysis/mdanalysis/pull/1652) Pytest Style coordinates/test_trz.py
* [#1653](https://github.com/MDAnalysis/mdanalysis/pull/1653) PEP8 fixes for coordinates/test_txyz.py
* [#1654](https://github.com/MDAnalysis/mdanalysis/pull/1654) Pytest Style coordinates/test_writer_registration.py
* [#1656](https://github.com/MDAnalysis/mdanalysis/pull/1656) Pytest Style coordinates/test_xyz.py
* [#1606](https://github.com/MDAnalysis/mdanalysis/pull/1606) Pytest Style topology/test_tprparser.py (WIP)
* [#1609](https://github.com/MDAnalysis/mdanalysis/pull/1609) Pytest Style TestEncore (WIP)
* [#1619](https://github.com/MDAnalysis/mdanalysis/pull/1619) Pytest Style core/test_updating_atomgroup.py (WIP)
* [#1635](https://github.com/MDAnalysis/mdanalysis/pull/1635) Pytest Style core/test_atomgroup.py (WIP)
* [#1642](https://github.com/MDAnalysis/mdanalysis/pull/1642) Remove yield based tests (WIP)
* [#1651](https://github.com/MDAnalysis/mdanalysis/pull/1651) Pytest Style coordinates/test_trj.py (WIP)
* [#1655](https://github.com/MDAnalysis/mdanalysis/pull/1655) Pytest Style coordinates/test_xdr.py (WIP)

That's it for now, see ya later!
