File guide
===============

Circular plate
--------------

A circular plate

- Sets 1
  1. Set 1 (edge_nodes): contains the nodes on the outer edge of the plate.
- Radius 5, thickness: 0.01.
- Material used in job file: IsoLE 1 d 1. E 10920e3. n 0.0 tAlpha 1.
- Pressure on elements: 1

Files:

- *circ_plate_08.in*: 601 nodes, 280 elements, sets 1.

- *circ_plate_06.in*: 1037 nodes, 492 elements

- *circ_plate_04.in*: 2641 nodes, 1280 elements

Cantilever ring
=============

A cantilever ring with one end clamped and a uniform line load on the other.

- Line load, up to 1000
- Sets 4 (NodalLoads cant be applied to sets yet so these have for now be applied manually to the correct nodes).
  1. Set 1 (clamped) The nodes to be clamped at one of the ring edges
  2. Set 2 (edge nodes) The nodes at the inner and outer edge that also are on the edge with the nodal loads. These should have fz*lz / 6 force.
  3. Set 3 (mid nodes) The nodes that are in the middle of two vertices of the element and on the edge with the nodal loads. These should have 2 * fz*lz / 3 force.
  4. Set 4 (double nodes) The rest of the nodes on the edge with the nodal loads. These should have fz*lz/3 force.
- Outer radius 10m
- Inner radius 6 m
- Thickness: 0.03
- Material used in job file: IsoLE 1 d 1. E 2.1e10. n 0.0 tAlpha 1.	

Files

- *cant_ring_12.in*: 581 nodes, 246 elements

- *cant_ring_08.in*: 1396 nodes, 630 elements

- *cant_ring_05.in*: 3417 nodes, 1600 elements

Pinched hemisphere
====================

Hemisphere with 18 degree hole at the pole.

- Sets: 8, the four different nodes to add force to and their respective nodes at the top
- Radius: 10 
- Thickness: 0.04
- Material: IsoLE 1 d 1. E 6.825e7. n 0.3 tAlpha 1.

*pinch_hemi_20.in*: 832 nodes, 384 elements

*pinch_hemi_15.in*: 1360 nodes, 640 elements

*pinch_hemi_12.in*: 2184 nodes, 1040 elements

Half cylinder
==============

Half cylinder with one clamped end and one free. The load is applied to the middle of the free end. (see 3.7 in Popular benchmark...).

- Sets 3
  1. Set 1 (Clamped) The nodes in the clamped frame
  2. Set 2 (Edges) The nodes where to specify the rotation
  3. Set 3 (P) The node where the force is applied
Radius: 100 (UNSURE ABOUT THIS, COULDNT FIND IN PDF)
Thickness: 1
Material: IsoLE 1 d 1. E 2.0685e7. n 0.3 tAlpha 1.

Files

- *half_cyl_100.in*: 693 nodes, 320 elements

- *half_cyl_75.in*: 1107 nodes, 520 elements

- *half_cyl_50.in*: 2665 nodes, 1280 elements

