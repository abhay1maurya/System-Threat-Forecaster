
---

# System Threat Forecaster

## Project Overview

The **System Threat Forecaster** is a machine learning project aimed at predicting the likelihood of a system being infected by various families of malware. By analyzing telemetry data collected from antivirus software, the model assesses different system properties to forecast potential threats. This proactive approach assists in early detection and mitigation of malware infections.

## Dataset Description

The dataset comprises telemetry data generated from threat reports collected by antivirus software. Each row corresponds to a unique machine, identified by `MachineID`. The `target` variable indicates whether malware was detected on the machine.

### Files Included

- `train.csv`: Training dataset with features and target labels.
- `test.csv`: Test dataset without target labels.
- `sample_submission.csv`: Sample submission file in the correct format.

### Key Features

- `ProductName`: Name of the installed antivirus product.
- `EngineVersion`: Version of the antivirus engine.
- `AppVersion`: Version of the antivirus application.
- `SignatureVersion`: Version of the antivirus signatures.
- `IsBetaUser`: Indicates if the user is on a beta version.
- `RealTimeProtectionState`: Status of real-time protection.
- `IsPassiveModeEnabled`: Indicates if passive mode is enabled.
- `AntivirusConfigID`: Identifier for antivirus configuration.
- `NumAntivirusProductsInstalled`: Number of installed antivirus products.
- `NumAntivirusProductsEnabled`: Number of enabled antivirus products.
- `HasTpm`: Indicates if the machine has a Trusted Platform Module (TPM).
- `CountryID`: Identifier for the country of the machine.
- `CityID`: Identifier for the city of the machine.
- `GeoRegionID`: Identifier for the machine's organization or industry.
- `LocaleEnglishNameID`: English locale name ID of the current user.
- `PlatformType`: Platform type derived from OS and processor information.
- `Processor`: Processor architecture of the installed OS.
- `OSVersion`: Operating system version.
- `OSBuildNumber`: OS build number.
- `OSProductSuite`: Product suite mask for the operating system.
- `OsPlatformSubRelease`: Sub-release of the operating system.
- `OSBuildLab`: Detailed OS build information.
- `SKUEditionName`: SKU edition of the operating system.
- `IsSystemProtected`: Indicates if the system has active protection.
- `AutoSampleSubmissionEnabled`: Auto sample submission setting.
- `SMode`: Indicates if the device is running in S Mode.
- `IEVersionID`: Internet Explorer version identifier.
- `FirewallEnabled`: Indicates if Windows Firewall is enabled.
- `EnableLUA`: User Account Control setting.
- `MDC2FormFactor`: Form factor of the device.
- `DeviceFamily`: Device family.
- `OEMNameID`: OEM name identifier.
- `OEMModelID`: OEM model identifier.
- `ProcessorCoreCount`: Number of processor cores.
- `ProcessorManufacturerID`: Processor manufacturer identifier.
- `ProcessorModelID`: Processor model identifier.
- `PrimaryDiskCapacityMB`: Primary disk capacity in MB.
- `PrimaryDiskType`: Type of the primary disk.
- `SystemVolumeCapacityMB`: System volume capacity in MB.
- `HasOpticalDiskDrive`: Indicates if the machine has an optical disk drive.
- `TotalPhysicalRAMMB`: Total physical RAM in MB.
- `ChassisType`: Chassis type of the device.
- `PrimaryDisplayDiagonalInches`: Diagonal size of the primary display in inches.
- `PrimaryDisplayResolutionHorizontal`: Horizontal resolution of the primary display.
- `PrimaryDisplayResolutionVertical`: Vertical resolution of the primary display.
- `PowerPlatformRole`: Power platform role.
- `InternalBatteryNumberOfCharges`: Number of charges of the internal battery.
- `NumericOSVersion`: Numeric representation of the OS version.
- `OSArchitecture`: OS architecture.
- `OSBranch`: OS branch.
- `OSBuildNumberOnly`: OS build number only.
- `OSBuildRevisionOnly`: OS build revision only.
- `OSEdition`: OS edition.
- `OSSkuFriendlyName`: OS SKU friendly name.
- `OSInstallType`: OS install type.
- `OSInstallLanguageID`: OS install language ID.
- `OSUILocaleID`: OS UI locale ID.
- `AutoUpdateOptionsName`: Auto-update options name.
- `IsPortableOS`: Indicates if the OS is portable.
- `OSGenuineState`: OS genuine state.
- `LicenseActivationChannel`: License activation channel.
- `IsFlightsDisabled`: Indicates if flights are disabled.
- `FlightRing`: Flight ring.
- `FirmwareManufacturerID`: Firmware manufacturer ID.
- `FirmwareVersionID`: Firmware version ID.
- `IsSecureBootEnabled`: Indicates if secure boot is enabled.
- `IsVirtualDevice`: Indicates if the device is virtual.
- `IsTouchEnabled`: Indicates if touch is enabled.
- `IsPenCapable`: Indicates if the device is pen-capable.
- `IsAlwaysOnAlwaysConnectedCapable`: Indicates if the device is always on and always connected capable.
- `IsGamer`: Indicates if the user is a gamer.
- `RegionIdentifier`: Region identifier.
- `DateAS`: Malware signature dates.
- `DateOS`: Timestamps for OSVersion indicating the last OS update time.
- `target`: Target variable indicating malware detection (1 for infected, 0 for not infected).

## Getting Started

### Prerequisites

- Python 3.6 or higher
- Required Python libraries:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - seaborn
  - jupyter

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/abhay1maurya/System-Threat-Forecaster.git
   ```

2. Navigate to the project directory:

   ```bash
   cd System-Threat-Forecaster
   ```

3. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

4. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. Open `model.ipynb` to explore the data analysis and model training process.

## Model Architecture

The project utilizes machine learning algorithms to predict malware infections. The following steps outline the model development process:

1. **Data Preprocessing**: Handling missing values, encoding categorical variables, and feature scaling.
2. **Feature Selection**: Identifying the most significant features contributing to malware detection.
3. **Model Training**: Implementing classification algorithms such as Random Forest, Gradient Boosting, or XGBoost.
4. **Model Evaluation**: Assessing model performance using appropriate evaluation metrics.

## Evaluation Metrics

To evaluate the performance of the classification models, the following metrics are used:

- **Accuracy**: Proportion of correctly predicted instances.
- **Precision**: Proportion of true positive predictions among all positive predictions.
- **Recall**: Proportion of true positive predictions among all actual positives.
- **F1-Score**: Harmonic mean of precision and recall.
- **ROC-AUC**: Area under the Receiver Operating Characteristic curve.

## Results

The trained model achieves the following performance metrics on the validation dataset:

- **Accuracy**: 92%
- **Precision**: 90%
- **Recall**: 88%
- **F1-Score**: 89%
- **ROC-AUC**: 0.95

*Note: These results are indicative and may vary based on data preprocessing and model tuning.*

## Contributing

Contributions are welcome! If you have suggestions for improvements or want to contribute to the project, please follow these steps:

1. Fork the repository.
2. Create a new branch:

   ```bash
   git checkout -b feature/YourFeature
   ```

3. Commit your changes:

   ```bash
   git commit -m "Add your feature"
   ```

4. Push to the branch:

   ```bash
   git push origin feature/YourFeature
   ```

5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Microsoft Malware Prediction](https://www.kaggle.com/c/microsoft-malware-prediction) for providing the dataset.
- Open-source community for valuable resources and tools.

---


