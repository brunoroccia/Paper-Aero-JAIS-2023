date:   05/27/2023
----------------------------------------------------------------------------------------------------------------------------------------------
This readme-file contains information for the results files of benchmark cases published in the article "A code-to-code benchmark for simulation tools based on the unsteady vortex-lattice method" calcutated with GSF-Aero
----------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------
The results files of benchmark cases
    benchmark_case_01 - Square flat wing under steady flow conditions
    benchmark_case_02 - Pitching wing
    benchmark_case_03 - Flapping/twisting wing
    benchmark_case_04 - Two-blade rotor in hover
    benchmark_case_05 - Two vertically-separated flapping/twisting wings
    benchmark_case_06 - Sandia 13.2 MW wind turbine rotor
are given in ASCII-format stored in text files which include the time histories of
    (1) vortex-ring ciruclations at control points of bounded vortex-lattice
    (2) vortex-ring pressure differences at control points of bounded vortex-lattice
    (3) nodal coordinates of the unbounded vortex-lattice, or wake.
----------------------------------------------------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------------------------------------------------
To facilitate reading the results files, their structure can be explained as follows:
----------------------------------------------------------------------------------------------------------------------------------------------
"benchmark_$number_of_benchmark_case$_uvlm_qs_nodal.dres"
    nodal coordinates (x1,x2,x3) of the bounded vortex-lattice for each time step with respect to the fixed reference coordinate system
        rows t      - results at time step t
        columns 3i  - coordinates of nodes i at time step t - [x1_1_t,x2_1_t,x3_1_t,...,x1_i_t,x2_i_t,x3_i_t,...,x1_nn_t,x2_nn,x3_nn_t]
An index-based assignment of the nodes to rings of the vortex-lattice is given in the file "benchmark_$number_of_benchmark_case$_uvlm_models.dres"
----------------------------------------------------------------------------------------------------------------------------------------------
"benchmark_$number_of_benchmark_case$_uvlm_dps_cp.dres"
    pressure differences (dps) at control points of each boundary elements of the bounded vortex-lattice for each time step
        rows t      - results at time step t
        columns i   - pressure differences at control point of boundary elements at time step t- [dps_1_t,...,dps_i_t,...,dps_nb_t]
----------------------------------------------------------------------------------------------------------------------------------------------
"benchmark_$number_of_benchmark_case$_uvlm_circs_cp.dres"
    vortex-ring circulations (circ) at control points of each boundary element of the bounded vortex-lattice for each time step
        rows t      - results at time step t
        columns i   - vortex-ring circulations at control point of boundary elements at time step t - [circ_1_t,...,circ_i_t,...,circ_nb_t]
----------------------------------------------------------------------------------------------------------------------------------------------
For more information regarding the results files, please feel free to contact us.