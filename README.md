# GEN3 Spherized URDF Models

Spherized collision geometry variants of the Kinova GEN3 7-DOF arm with different fidelity levels for collision solver benchmarking.

## Contents

- **urdf/**: URDF files with spherized collision geometry
- **meshes/**: Original mesh files (STL)

## Fidelity Levels

| Level | Collision Spheres | File | Visual Variant |
|-------|-------------------|------|---------------|
| fid0  | 8 (minimal)       | `GEN3_URDF_V12_fid0.urdf` | `GEN3_URDF_V12_fid0_with_sphere_visuals.urdf` |
| fid1  | 28                | `GEN3_URDF_V12_fid1.urdf` | `GEN3_URDF_V12_fid1_with_sphere_visuals.urdf` |
| fid2  | 43                | `GEN3_URDF_V12_fid2.urdf` | `GEN3_URDF_V12_fid2_with_sphere_visuals.urdf` |
| fid3  | 65                | `GEN3_URDF_V12_fid3.urdf` | `GEN3_URDF_V12_fid3_with_sphere_visuals.urdf` |
| fid4  | 71                | `GEN3_URDF_V12_fid4.urdf` | `GEN3_URDF_V12_fid4_with_sphere_visuals.urdf` |
| fid5  | 73                | `GEN3_URDF_V12_fid5.urdf` | `GEN3_URDF_V12_fid5_with_sphere_visuals.urdf` |
| fid6  | 1037 (ultra-high) | `GEN3_URDF_V12_fid6.urdf` |

## File Variants

### Plain Files (e.g., `GEN3_URDF_V12_fid0.urdf`)
- Contains original mesh visuals + collision spheres

### Visual Variants (e.g., `GEN3_URDF_V12_fid0_with_sphere_visuals.urdf`)
- Shows blue sphere visuals instead of meshes
- Collision geometry remains identical to plain files
