# GEN3 Spherized URDF Models

Spherized collision geometry variants of the Kinova GEN3 7-DOF arm with different fidelity levels for collision solver benchmarking.

## Contents

- **urdf/**: URDF files with spherized collision geometry
- **meshes/**: Original mesh files (STL format)

## Fidelity Levels

| Level | Collision Spheres | File | Visual Variant |
|-------|-------------------|------|---------------|
| fid0  | 8 (minimal)       | `GEN3_URDF_V12_fid0.urdf` | `GEN3_URDF_V12_fid0_with_sphere_visuals.urdf` |
| fid1  | 28                | `GEN3_URDF_V12_fid1.urdf` | `GEN3_URDF_V12_fid1_with_sphere_visuals.urdf` |
| fid2  | 43                | `GEN3_URDF_V12_fid2.urdf` | `GEN3_URDF_V12_fid2_with_sphere_visuals.urdf` |
| fid3  | 65                | `GEN3_URDF_V12_fid3.urdf` | `GEN3_URDF_V12_fid3_with_sphere_visuals.urdf` |
| fid4  | 71                | `GEN3_URDF_V12_fid4.urdf` | `GEN3_URDF_V12_fid4_with_sphere_visuals.urdf` |
| fid5  | 73                | `GEN3_URDF_V12_fid5.urdf` | `GEN3_URDF_V12_fid5_with_sphere_visuals.urdf` |
| fid6  | 1037 (ultra-high) | `GEN3_URDF_V12_fid6.urdf` | `GEN3_URDF_V12_fid6_with_sphere_visuals.urdf` |
| fid7  | 1067 (ultra-high) | `GEN3_URDF_V12_fid7.urdf` | (not included) |

## File Variants

### Plain Files (e.g., `GEN3_URDF_V12_fid0.urdf`)
- Contains original mesh visuals + collision spheres
- Use for visualization and physics simulation

### Visual Variants (e.g., `GEN3_URDF_V12_fid0_with_sphere_visuals.urdf`)
- Shows blue sphere visuals instead of meshes
- Collision geometry remains identical to plain files
- Useful for comparing sphere approximations visually

## Usage

### In Gazebo
```bash
gazebo urdf/GEN3_URDF_V12_fid0.urdf
```

### In RViz
```bash
rviz -d config.rviz &
# Then load the URDF model
```

### For Collision Solver Testing
All files contain embedded sphere collision geometry. The collision spheres are independent of visual representation — use either variant for collision testing.

## Directory Structure

```
gen3_spherized/
├── README.md
├── urdf/
│   ├── GEN3_URDF_V12_fid0.urdf
│   ├── GEN3_URDF_V12_fid0_with_sphere_visuals.urdf
│   ├── GEN3_URDF_V12_fid1.urdf
│   ├── GEN3_URDF_V12_fid1_with_sphere_visuals.urdf
│   └── ... (fid2-fid7 variants)
└── meshes/
    ├── base_link.STL
    ├── shoulder_link.STL
    ├── half_arm_1_link.STL
    ├── half_arm_2_link.STL
    ├── forearm_link.STL
    ├── spherical_wrist_1_link.STL
    ├── spherical_wrist_2_link.STL
    ├── bracelet_no_vision_link.STL
    ├── bracelet_with_vision_link.STL
    └── end_effector_link.STL
```

## Notes

- Collision geometry: Spheres only (replaced from original mesh-based collisions)
- Visual geometry: Meshes (plain files) or blue spheres (visual variants)
- All files maintain relative path references (`../meshes/...`)
- Suitable for benchmarking collision detection algorithms with varying approximation fidelities
