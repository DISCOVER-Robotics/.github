<div align="left">

<img src="https://raw.githubusercontent.com/DISCOVER-Robotics/.github/feat/update-profile-readme/assets/discover-header-logo-dark.svg" width="380" height="211" alt="DISCOVER Robotics">

## About us

DISCOVER Robotics develops embodied intelligence and robotics technology across hardware, motion control, perception, manipulation learning, and simulation. Our open-source projects connect research ideas with dependable real-world robot applications.

[![Website](https://img.shields.io/badge/Website-discover--robotics.com-111827?style=flat-square&logo=googlechrome&logoColor=white)](https://www.discover-robotics.com/)
[![Documentation](https://img.shields.io/badge/Documentation-Docs-2563eb?style=flat-square&logo=readthedocs&logoColor=white)](https://docs.discover-robotics.com/document/)
[![GitHub](https://img.shields.io/badge/GitHub-DISCOVER--Robotics-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/DISCOVER-Robotics)

</div>

## Open source

| Focus | Projects | Description |
| --- | --- | --- |
| **Robot platforms** | [AIRBOT Play Hardware](https://github.com/DISCOVER-Robotics/AIRBOT-Play-Hardware) · [AIRBOT-Play-Hardware-with-Moveit2](https://github.com/DISCOVER-Robotics/AIRBOT-Play-Hardware-with-Moveit2) | AIRBOT Play hardware interfaces and MoveIt 2 integration |
| **Simulation** | [DISCOVERSE](https://github.com/DISCOVER-Robotics/DISCOVERSE) · [Mosaic](https://github.com/DISCOVER-Robotics/Mosaic) · [WorldModelSim](https://github.com/DISCOVER-Robotics/WorldModelSim) | Simulation, world-model, and data tools for embodied intelligence |
| **Manipulation & learning** | [Imitate-All](https://github.com/DISCOVER-Robotics/Imitate-All) · [3D-Diffusion-Policy](https://github.com/DISCOVER-Robotics/3D-Diffusion-Policy) · [auto-atomic-operation](https://github.com/DISCOVER-Robotics/auto-atomic-operation) | Imitation learning, diffusion policies, and atomic operation frameworks |
| **Perception & data** | [Medusa](https://github.com/DISCOVER-Robotics/Medusa) · [GraspNetAPI](https://github.com/DISCOVER-Robotics/GraspNetAPI) · [data-engine](https://github.com/DISCOVER-Robotics/data-engine) | Visual perception, grasping data, and data engineering |
| **Control & SDK** | [sdk](https://github.com/DISCOVER-Robotics/sdk) · [arm-control](https://github.com/DISCOVER-Robotics/arm-control) · [control](https://github.com/DISCOVER-Robotics/control) | Robot SDKs, control, and motion-planning components |

## Featured demos

| Category | Demo | Description |
| --- | --- | --- |
| **Dual-arm manipulation** | [PTK Cloth Folding](#ptk-cloth-folding-demo) | A dual-AIRBOT Play demonstration using a PI0.5 policy to fold a T-shirt. Includes workstation options, model resources, camera layout, and startup overview. |
| **Vision & simulation** | [Keyboard Visual Grasp](#keyboard-visual-grasp-demo) | A single-arm DISCOVERSE simulation for visual block detection, segmentation, grasp-pose estimation, and pick-and-place using keyboard commands. Simulation only; no real robot control. |

### PTK Cloth Folding Demo

This dual-arm AIRBOT Play demo uses a PI0.5 policy to fold a plain T-shirt. Two workstation layouts are described: a TV-backed setup for visual-background demonstrations and a simplified white-table setup.

- **Validated software baseline:** AIRBOT 5.1.6 (`airbot-configure`, `airbot_py`, and `airbot_fsm`). Do not substitute V5.2 `arm_sdk` / `airbot-arm` commands.
- **Hardware:** 2 × AIRBOT Play arms, 2 grippers, 2 wrist cameras, and 1 environment camera. Camera order is environment, left wrist, right wrist.
- **Code:** [Robot-K/Openpi_RL](https://github.com/Robot-K/Openpi_RL)
- **Pre-trained policy:** [policy-v3-wospatiodelta-iter4-tv2-280000](https://huggingface.co/xiaoleezuishuai/policy-v3-wospatiodelta-iter4-tv2-280000)
- **Optional training data:** [airbot-fold-cloth-mcap](https://huggingface.co/datasets/xiaoleezuishuai/airbot-fold-cloth-mcap)
- **Setup references:** [PTK data collection](https://docs.discover-robotics.com/document/airbot-play/hardware-driver/tutorials/data-collection.html) · [PI0.5 model reproduction](https://docs.discover-robotics.com/document/airbot-play/hardware-driver/tutorials/model-reproduction/pi0.5.html) · [AIRBOT Play 5.1.6 release](https://docs.discover-robotics.com/document/airbot-play/changelog.html#20250623)

The model can be downloaded with Hugging Face CLI:

```bash
uvx --from 'huggingface_hub>=1.0' hf download \
  xiaoleezuishuai/policy-v3-wospatiodelta-iter4-tv2-280000 \
  --local-dir "$HOME/tv_fold_demo/policy_v3_wospatiodelta_iter4_tv2"
```

### Keyboard Visual Grasp Demo

This single-arm demo runs the visual grasp pipeline in DISCOVERSE simulation. It shows a third-person scene and an end-effector camera view, and demonstrates object detection, MobileSAM segmentation, grasp-pose estimation, and simulated pick-and-place. The keyboard-only workflow does not start speech recognition and does not connect to or control a physical robot.

- **Validated software baseline:** Ubuntu 22.04 with Python 3.10 (Python 3.10–3.12 supported by the installer); project robot SDK/service baseline is 5.2.2.
- **Install and launch:**

  ```bash
  ./install_keyboard.sh
  ./run_keyboard.sh
  ```

- **Example commands:** `抓取蓝色积木`, `抓取绿色积木`, `打开夹爪`, `闭合夹爪`, `回到观察位`, `拍照`, and `预测位姿`.
- **Source availability:** the current demo is maintained in a local project directory; a public source-repository link will be added when one is available.

Browse all repositories: [github.com/DISCOVER-Robotics?tab=repositories](https://github.com/DISCOVER-Robotics?tab=repositories)

## Resources

- [DISCOVER Robotics Documentation Center](https://docs.discover-robotics.com/document/): product manuals, SDKs, quick starts, and development guides
- [Official website](https://www.discover-robotics.com/): products, solutions, and services
- [DISCOVER Lab](https://www.discover-lab.com/): research and development community
- [GitHub organization](https://github.com/DISCOVER-Robotics): browse projects, open issues, and collaborate

## Contributing

We welcome developers, researchers, and robotics enthusiasts. Before contributing, please read the target repository's `README`, contribution guide, and license, then open an Issue or Pull Request.

<div align="center">

<a href="https://github.com/DISCOVER-Robotics"><img src="https://img.shields.io/badge/Explore%20our%20repositories-181717?style=for-the-badge&logo=github&logoColor=white" alt="Explore repositories"></a>

<br><br>

© DISCOVER Robotics

</div>
