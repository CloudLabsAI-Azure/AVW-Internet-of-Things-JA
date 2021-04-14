# ���K 4: Azure IoT Edge ���g���n�߂�

## �V�i���I

�c��Ȑ��̃f�o�C�X���f�v���C����Ă���A��ʂ̃f�[�^�����W����ăN���E�h�ɑ��M����Ă��܂��BEdge �ɃC���e���W�F���X�𓱓����邱�Ƃ͉\�ł���?

Fabrikam, Inc. �́AIoT Edge �Q�[�g�E�F�C �f�o�C�X���g�p���āA�����ɏ������邽�߂ɃC���e���W�F���X�̈ꕔ���G�b�W�ɓ����������ƍl���Ă��܂��B�f�[�^�̈ꕔ�͈��������N���E�h�ɑ��M����܂��B����ɁA�f�[�^ �C���e���W�F���X�� IoT Edge �ɓ������邱�ƂŁA���[�J�� �l�b�g���[�N���n��ȏꍇ�ł��A�f�[�^���������Đv���ɑΉ��ł���悤�ɂȂ�܂��B

����܂łɁAAzure IoT Edge �\�����[�V�����̃v���g�^�C�s���O���s���Ă���ꂽ���Ƃł��傤�B�܂��AStream Analytics ���W���[�����f�o�C�X�Ƀf�v���C���܂��B���̃��W���[�����g�p���āA���ω��x���v�Z���A�v���Z�X����l�𒴂����ꍇ�ɃA���[�g�ʒm�𐶐����܂��B

## �T�v

���̉��K�ł́AStream Analytics ���W���[���� Edge �f�o�C�X�Ƀf�v���C���A�v���Z�X����l�𒴂����ꍇ�ɃA���[�g�ʒm�����������悤�ɐݒ肵�܂��B���̃��{�̖ړI�ɉ����āAIoT Edge �f�o�C�X�Ƃ��č\�����ꂽ�A�쐬�ς� Linux �x�[�X�� Azure VM ���񋟂���܂��B

���̉��K�̈�Ƃ��āA���̃^�X�N�����s���܂��B

* IoT Edge VM �ɐڑ�����
* Edge ���W���[���� Edge �f�o�C�X�ɒǉ�����
* Azure Stream Analytics Edge ���W���[���� Edge �f�o�C�X�Ƀf�v���C����

Azure IoT Edge �́A�N���E�h�Ŏ��s�����N���E�h �T�[�r�X�ƁA�f�o�C�X�Ŏ��s����郉���^�C���̑g�ݍ��킹�ł��B�����^�C�����n�����A�f�o�C�X��̃��[�N�t���[���Ǘ����܂��B���[�N�t���[�́A����̏����Ń����N���ăG���h�c�[�G���h�̃V�i���I���쐬�����A�̃R���e�i�[�ō\������܂��BIoT Edge �� IoT Hub �ɂ���ĊǗ�����܂��BAzure IoT Edge ���g�p����ƁA�N���E�h �T�[�r�X���g�p���ĊJ�����ꂽ�G�b�W �f�o�C�X�Ń��[�N���[�h�����s�ł��܂��B���[�N���[�h�́ADocker �݊��R���e�i�[���g�p���ăf�v���C���ꂽ���W���[���ł��B���W���[���́A�l�H�m�\�A�v���P�[�V�����AAzure ����уT�[�h�p�[�e�B�̃T�[�r�X�A�܂��̓r�W�l�X ���W�b�N�ł���\��������܂��B�ڂ��� IoT Edge �̐����ɂ��ẮA���̃����N�Ɉړ��ł��܂��B```https://docs.microsoft.com/en-us/azure/iot-edge/about-iot-edge```

## �\�����[�V���� �A�[�L�e�N�`��
 
  ![Lab 04 �A�[�L�e�N�`��](media/lab4_architecture.png)

### �^�X�N 1: IoT Edge VM �ɐڑ�����

���̃^�X�N�ł́AIoT Edge VM �ɐڑ����AAzure IoT Edge ���f�o�C�X�Ŏ��s����Ă��邩�ǂ������m�F���܂��B

1. Azure Portal ���j���[�ŁA**[���\�[�X �O���[�v]** ���N���b�N���܂��B
 
1. **iot-{deployment-id}** ���\�[�X �O���[�v����AIoT Edge ���z�}�V�� **linuxagentvm-{deployment-id}** ���N���b�N���܂��B

1. **[�T�v]** �E�B���h�E�̏㕔�ɂ��� **[�ڑ�]** ���N���b�N���Ă���A**[SSH]** ���N���b�N���܂��B

1. **[�ڑ�]** �y�C���� **[4.�ȉ��̃T���v�� �R�}���h�����s���� VM �ɐڑ�]** �̉��ɂ���T���v�� �R�}���h���R�s�[���܂��B

    ����́AVM �� IP �A�h���X�ƊǗ��҃��[�U�[�����܂މ��z�}�V���ɐڑ����邽�߂Ɏg�p�ł���T���v�� SSH �R�}���h�ł��B�R�}���h�́A`ssh demouser@52.170.205.79` �Ɠ��l�Ƀt�H�[�}�b�g����K�v������܂��B

    > **��**: �R�s�[�����T���v�� �R�}���h�ɂ́A**-i <private key path>** ���܂܂�Ă��܂��B�e�L�X�g �G�f�B�^�[���g�p���ăR�}���h�̂��̕������폜���Ă���A�X�V���ꂽ�R�}���h���N���b�v�{�[�h�ɃR�s�[���܂��B
 
1. **```https://shell.azure.com```** �Ɉړ����� Azure Cloud Shell���J���A**Bash** ��I�����܂��B

1. **[�ڍאݒ��\��]** ���N���b�N���āA���̏ڍׂ���͂��܂��B

   * ���\�[�X �O���[�v : **[�����̂��̂��g�p]** -> **iot-{deployment-id}** ��I�����܂�
   * �X�g���[�W �A�J�E���g: **[�V�K�쐬]** ��I�����A**cloudstore{deployment-id}** �Ɠ��͂��܂�
   * �t�@�C�����L: **[�V�K�쐬]** ��I�����A**blob** �Ɠ��͂��܂�
   
     >   **��**: - [���̏ڍ�] �y�[�W���� **deployment-id** �̏ڍׂ��擾�ł��܂��B
        
   ![�X�g���[�W �A�J�E���g���쐬���邽�߂̑I���p�X��\�����Ă��� Azure �|�[�^���̃X�N���[���V���b�g�B](media/storageaccount01.png)

1. Azure Cloud Shell �̃R�}���h �v�����v�g�ŁA�X�V���� `ssh` �R�}���h���e�L�X�g �G�f�B�^�[�ɓ\��t���āA**Enter** �L�[�������܂��B

1. **Are you sure you want to continue connecting?** �Ƃ������b�Z�[�W���\�����ꂽ��A`yes` �Ɠ��͂��A**Enter** �L�[�������܂��B

1. �p�X���[�h�̓��͂����߂�ꂽ��A**Password.1!!** �Ɠ��͂��A**Enter** �L�[�������܂��B

   ![linuxagent ���z�}�V���֐ڑ����B](media/vmlogin.png)

1. �ڑ�����ƁA�^�[�~�i���̃R�}���h �v�����v�g���ς��ALinux VM �̖��O�����̂悤�ɕ\������܂��B

    ```cmd/sh
    demouser@linuxagentvm-{deployment-id}:~$
    ```

    ����ɂ��A�ڑ����Ă��� VM ���킩��܂��B

    > **�d�v:**�ڑ�����ƁAEdge VM �̖��K�p�� OS �A�b�v�f�[�g�ɂ��Ă̒ʒm���󂯎��\��������܂��B  ���̂��Ƃ̓��{�̖ړI�ɉ����Ė������Ă��܂����A���ғ����ł́AEdge �f�o�C�X����ɍŐV�̏�ԂɕۂK�v������܂��B

1. Azure IoT Edge �����^�C���� VM �ɃC���X�g�[������Ă��邱�Ƃ��m�F����ɂ́A���̃R�}���h�����s���܂��B

    ```cmd/sh
    iotedge version
    ```

    ���̃R�}���h�́A���z�}�V���Ɍ��݃C���X�g�[������Ă��� Azure IoT Edge �����^�C���̃o�[�W�������o�͂��܂��B
    IoT Edge �f�o�C�X�ɂ́AIoT Edge �����^�C�����C���X�g�[������Ă��܂��BIoT Edge �����^�C���́A�f�o�C�X�� IoT Edge �f�o�C�X�ɕς���v���O�����̃R���N�V�����ł��BIoT Edge �����^�C�� �R���|�[�l���g�ɂ��A�W���I�ɁAIoT Edge �f�o�C�X�̓G�b�W�Ŏ��s����R�[�h����M���āA���ʂ� IoT Hub �ƒʐM�ł��܂��B

### �^�X�N 2: Edge ���W���[���� Edge �f�o�C�X�ɒǉ�����

���̉��K�ł́ASimulated Temperature Sensor ���J�X�^�� IoT Edge ���W���[���Ƃ��Ēǉ����A�����W�J���� IoT Edge �f�o�C�X�Ŏ��s���܂��B

IoT Edge ���W���[���́A�R���e�i�[�Ƃ��Ď����������s�\�p�b�P�[�W�ł��B

IoT Edge ���W���[������A�N���E�h ���[�N���[�h���f�v���C���āAIoT �f�o�C�X�Œ��ڎ��s�ł��܂��BIoT Edge ���W���[���́AIoT Edge �ɂ���ĊǗ������ŏ��̌v�Z�P�ʂł��BIoT Edge ���W���[�����g�p����ƁA�N���E�h�ł͂Ȃ��f�o�C�X��̃f�[�^�𕪐͂ł��܂��B���[�N���[�h�̈ꕔ���G�b�W�Ɉړ����邱�ƂŁA�f�o�C�X�̓N���E�h�ւ̃��b�Z�[�W�̑��M�ɔ�₷���Ԃ�Z�k���A�C�x���g�ɂ��v���ɑΉ��ł��܂��B

1. �K�v�ɉ����āAAzure �A�J�E���g�̎��i�����g�p���� Azure Portal �Ƀ��O�C�����܂��B
 
1. [���\�[�X] �O���[�v �^�C���ŁAIoT Hub ���J���ɂ́A**iothub-{deployment-id}** ���N���b�N���܂��B

1. **IoT Hub** �u���[�h�̍����ɂ��� **[Automatic Device Management (�����f�o�C�X�Ǘ�)]** �̉��ŁA**[IoT Edge]** ���N���b�N���܂��B

1. IoT Edge �f�o�C�X�̃��X�g�ŁA**turbine-06** ���N���b�N���܂��B

1. **turbine-06** �u���[�h�ŁA**[���W���[��]** �^�u�Ƀf�o�C�X�p�Ɍ��ݍ\������Ă��郂�W���[���̃��X�g���\������Ă��邱�Ƃɒ��ӂ��Ă��������B

    ���݁AIoT Edge �f�o�C�X�́AIoT Edge �����^�C���̈ꕔ�ł��� Edge �G�[�W�F���g (`$edgeAgent`) ���W���[���� Edge Hub (`$edgeHub`) ���W���[���݂̂ō\������Ă��܂��B

1. **turbine-06** �u���[�h�̏㕔�ɂ��� **[���W���[����ݒ�]** ���N���b�N���܂��B

1. **[Set modules on device: turbine-06]** �u���[�h�ŁA**IoT Edge Modules** �Z�N�V�����������܂��B

1. **[IoT Edge ���W���[��]** �̉��ŁA**[�ǉ�]** ���N���b�N���Ă���A**[IoT Edge ���W���[��]** ���N���b�N���܂��B

1. **[Add IoT Edge Module]** �E�B���h�E�� **[IoT Edge Module Name]** �̉��ɁA**turbinesensor** �Ɠ��͂��܂�

    �J�X�^�� ���W���[���Ɂuturbinesensor�v�Ƃ������O��t���܂�

1. **[�C���[�W URI]** �ŁA**asaedgedockerhubtest/asa-edge-test-module:simulated-temperature-sensor** �Ɠ��͂��܂��B

    > **��**: ���̃C���[�W�́A���̃e�X�g �V�i���I���T�|�[�g���邽�߂ɐ��i�O���[�v�ɂ���Ē񋟂��ꂽ Docker Hub ��̌��J�C���[�W�ł��B

1. �I�������^�u��ύX����ɂ́A**[Module Twin Settings (���W���[�� �c�C���ݒ�)]** ���N���b�N���܂��B

1. ���W���[�� �c�C���ɕK�v�ȃv���p�e�B���w�肷��ɂ́A���� JSON ����͂��܂��B

    ```json
    {
        "EnableProtobufSerializer": false,
        "EventGeneratingSettings": {
            "IntervalMilliSec": 500,
            "PercentageChange": 2,
            "SpikeFactor": 2,
            "StartValue": 68,
            "SpikeFrequency": 20
        }
    }
    ```

    ���� JSON �́A���W���[�� �c�C���̖ړI�̃v���p�e�B��ݒ肷�邱�Ƃ� Edge ���W���[�����\�����܂��B

1. �u���[�h�̉����ɂ��� **[�ǉ�]** ���N���b�N���܂��B

1. **[Set modules on device: turbine-06]** �u���[�h�̉����ɂ��� **[Next: Routes >]** ���N���b�N���܂��B

1. ���胋�[�g�����łɐݒ肳��Ă��邱�Ƃɒ��ڂ��Ă��������B

    * ���O: **route**
    * �l: `FROM /messages/* INTO $upstream`

    ���̃��[�g�́AIoT Edge �f�o�C�X��̂��ׂẴ��W���[������ IoT Hub �ɂ��ׂẴ��b�Z�[�W�𑗐M���܂�

1. **[Review + create]** ���N���b�N���܂��B

1. **[Deployment]** �ŁA�\�����ꂽ�f�v���C �}�j�t�F�X�g�������̎��Ԃ�����Ċm�F���܂��B 

    �����̂Ƃ���AIoT Edge �f�o�C�X�̃f�v���C �}�j�t�F�X�g�� JSON �Ƃ��ăt�H�[�}�b�g����Ă��邽�߁A���ɓǂ݂₷���Ȃ��Ă��܂��B

    `properties.desired` �Z�N�V�����̉��ɂ́AIoT Edge �f�o�C�X�Ƀf�v���C����� IoT Edge ���W���[����錾���� `modules` �Z�N�V����������܂��B����ɂ́A�R���e�i�[ ���W�X�g���̎��i�����܂ނ��ׂẴ��W���[���̃C���[�W URI ���܂܂�܂��B

    ```json
    {
        "modulesContent": {
            "$edgeAgent": {
                "properties.desired": {
                    "modules": {
                        "turbinesensor": {
                            "settings": {
                                "image": "asaedgedockerhubtest/asa-edge-test-module:simulated-temperature-sensor",
                                "createOptions": ""
                            },
                            "type": "docker",
                            "version": "1.0",
                            "status": "running",
                            "restartPolicy": "always"
                        },
    ```

    JSON �̉����ɂ́AEdge Hub �ɕK�v�ȃv���p�e�B���܂� **$edgeHub** �Z�N�V����������܂��B���̃Z�N�V�����ɂ́A���W���[���Ԃ���� IoT Hub �ւ̃C�x���g�̃��[�e�B���O�̂��߂̃��[�e�B���O�\�����܂܂�Ă��܂��B

    ```json
        "$edgeHub": {
            "properties.desired": {
                "routes": {
                  "route": "FROM /messages/* INTO $upstream"
                },
                "schemaVersion": "1.0",
                "storeAndForwardConfiguration": {
                    "timeToLiveSecs": 7200
                }
            }
        },
    ```

    JSON �̂���ɉ��ɂ́A**turbinesensor** ���W���[���̃Z�N�V����������܂��B�����ŁA`properties.desired` �Z�N�V�����ɂ́AEdge ���W���[���̍\���ɕK�v�ȃv���p�e�B���܂܂�Ă��܂��B

    ```json
                },
                "turbinesensor": {
                    "properties.desired": {
                        "EnableProtobufSerializer": false,
                        "EventGeneratingSettings": {
                            "IntervalMilliSec": 500,
                            "PercentageChange": 2,
                            "SpikeFactor": 2,
                            "StartValue": 68,
                            "SpikeFrequency": 20
                        }
                    }
                }
            }
        }
    ```

1. �f�o�C�X�̃��W���[���̐ݒ���I������ɂ́A�u���[�h�̉����ɂ��� **[�쐬]** ���N���b�N���܂��B

1. **turbine-06** �u���[�h�� **[Modules]** �̉��ŁA**turbinesensor** �����X�g�����悤�ɂȂ������Ƃɒ��ڂ��Ă��������B

    > **��**: ���߂ă��X�g���ꂽ���W���[����\������ɂ́A**[�ēǂݍ���]** ���N���b�N����K�v������ꍇ������܂��B

    **turbinesensor** �� RUNTIME STATUS ���񍐂���Ă��Ȃ����ƂɋC�t���ꍇ������܂��B

1. �u���[�h�̏㕔�ŁA**[�ēǂݍ���]** ���N���b�N���܂��B

1. **turbinesensor** ���W���[���� **RUNTIME STATUS** �� **running** �ɐݒ肳��Ă��邱�Ƃɒ��ڂ��Ă��������B

    ����ł��l���񍐂���Ȃ��ꍇ�́A���΂炭�҂��Ă���A�u���[�h���ēx�A�ēǂݍ��݂��Ă��������B
 
1. Cloud Shell �Z�b�V�������J���܂� (�܂��J���Ă��Ȃ��ꍇ)�B

    `vm-iot-edge-{deployment-id}` ���z�}�V���ɐڑ����Ȃ��Ȃ����ꍇ�́A�ȑO�Ɠ��l�� **SSH** ���g�p���Đڑ����܂��B

1. Cloud Shell �R�}���h �v�����v�g�ŁAIoT Edge �f�o�C�X�Ō��ݎ��s���Ă��郂�W���[�������X�g����ɂ́A���̃R�}���h����͂��܂��B

    ```cmd/sh
    iotedge list
    ```

1. �R�}���h�̏o�͎͂��̂悤�ɂȂ�܂��B 

    ```cmd/sh
    demouser@linuxagentvm-{deployment-id}:~$ iotedge list
    NAME             STATUS           DESCRIPTION      CONFIG
    edgeHub          running          Up a minute      mcr.microsoft.com/azureiotedge-hub:1.0
    edgeAgent        running          Up 26 minutes    mcr.microsoft.com/azureiotedge-agent:1.0
    turbinesensor    running          Up 34 seconds    asaedgedockerhubtest/asa-edge-test-module:simulated-temperature-sensor
    ```

    ���s���̃��W���[���� 1 �Ƃ��� `turbinesensor` �����X�g����Ă��邱�Ƃɒ��ڂ��Ă��������B

1. ���W���[�� ���O��\������ɂ́A���̃R�}���h����͂��܂��B

    ```cmd/sh
    iotedge logs turbinesensor
    ```

    �R�}���h�̏o�͎͂��̂悤�ɂȂ�܂��B

    ```cmd/sh
    demouser@linuxagentvm-{deployment-id}:~$ iotedge logs turbinesensor
    11/14/2019 18:05:02 - Send Json Event : {"machine":{"temperature":41.199999999999925,"pressure":1.0182182583425192},"ambient":{"temperature":21.460937846433808,"humidity":25},"timeCreated":"2019-11-14T18:05:02.8765526Z"}
    11/14/2019 18:05:03 - Send Json Event : {"machine":{"temperature":41.599999999999923,"pressure":1.0185790159334602},"ambient":{"temperature":20.51992724976499,"humidity":26},"timeCreated":"2019-11-14T18:05:03.3789786Z"}
    11/14/2019 18:05:03 - Send Json Event : {"machine":{"temperature":41.999999999999922,"pressure":1.0189397735244012},"ambient":{"temperature":20.715225311096397,"humidity":26},"timeCreated":"2019-11-14T18:05:03.8811372Z"}
    ```

    �C�ӂ� Edge ���W���[���̃��W���[�� ���O��\������ɂ́A`iotedge logs` �R�}���h���g�p�ł��܂��B

1. Simulated Temperature Sensor ���W���[���́A500 �̃��b�Z�[�W�𑗐M������ɒ�~���܂��B���̃R�}���h�����s����ƁA�ċN���ł��܂��B

    ```cmd/sh
    iotedge restart turbinesensor
    ```

    ���������W���[�����ċN������K�v�͂���܂��񂪁A��Ńe�����g���̑��M����~�����ꍇ�́ACloud Shell �ɖ߂�AEdge VM �� SSH �Őڑ����A���̃R�}���h�����s���ă��Z�b�g���܂��B���Z�b�g�����ƁA���W���[���̓e�����g���̑��M���ĊJ���܂��B

### �^�X�N 3: Azure Stream Analytics Edge ���W���[���� IoT Edge ���W���[���Ƃ��ăf�v���C����

**turbinesensor** ���W���[���� IoT Edge �f�o�C�X�Ƀf�v���C����Ď��s���ꂽ�̂ŁAIoT Hub �ɑ��M����O�ɁAIoT Edge �f�o�C�X���̂Ń��b�Z�[�W�������ł��� Stream Analytics ���W���[����ǉ��ł��܂��B

#### Stream Analytics �W���u���m�F����

1. ���\�[�X �O���[�v �^�C���ŁA**iot-{deployment-id}** ���N���b�N���A**iotedge-streamjob-{deployment-id}** �Ƃ��� Stream Analytics �W���u��I�����܂��B

1. ���ɁA�u���[�h�̍����ɂ��� **[�W���u �g�|���W]** �ŁA**[����]** ��I�����A1 �̓��̓W���u **temperature** �����łɒ�`����Ă��邱�Ƃ��m�F���܂��B

1. ���ɁA**[�W���u �g�|���W]** �̉��� **[�o��]** ��I�����A1 �̏o�̓W���u **alert** �����łɒ�`����Ă��邱�Ƃ��m�F���܂��B

1. �����̃i�r�Q�[�V���� ���j���[�� **[�\��]** �ŁA[Storage account settings (�X�g���[�W �A�J�E���g�̐ݒ�)] ���N���b�N���܂��Biotstorage{deployment-id} �X�g���[�W �A�J�E���g���ǉ�����Ă��邱�Ƃ��m�F���܂��B

#### Stream Analytics �W���u���f�v���C����

1. Azure Portal �ŁA**iothub-{deployment-id}** IoT Hub ���\�[�X�Ɉړ����܂��B

1. �����̃i�r�Q�[�V���� ���j���[�� **[Automatic Device Management (�����f�o�C�X�Ǘ�)]** �ŁA**[IoT Edge]** ���N���b�N���܂��B

1. **[�f�o�C�X ID]** �̉��ŁA**turbine-06** ���N���b�N���܂��B

1. **turbine-06** �E�B���h�E�̏㕔�ɂ��� **[���W���[����ݒ�]** ���N���b�N���܂��B

1. **[Set modules on device: turbine-06]** �E�B���h�E�ŁA**IoT Edge Modules** �Z�N�V�����������܂��B

1. **[IoT Edge ���W���[��]** �̉��ŁA**[�ǉ�]** ���N���b�N���Ă���A**[Azure Stream Analytics ���W���[��]** ���N���b�N���܂��B

1. **[Edge deployment]** �E�B���h�E�� **[Subscription]** �̉��ŁA���̃R�[�X�Ɏg�p���Ă���T�u�X�N���v�V�������I������Ă��邱�Ƃ��m�F���܂��B

1. **[Edge job (Edge �W���u)]** �h���b�v�_�E���ŁA**iotedge-streamjob-{deployment-id}** Steam Analytics �W���u���I������Ă��邱�Ƃ��m�F���܂��B

    > **��**: �W���u�͂��łɑI������Ă���\��������܂����A**[�ۑ�]** �{�^���͖����ɂȂ��Ă��܂��B**[Edge job (Edge �W���u)]** �h���b�v�_�E����������x�J���A**iotedge-streamjob-{deployment-id}** �W���u��������x�I�����܂��B���ɁA**[�ۑ�]** �{�^�����L���ɂȂ�܂��B

1. �E�B���h�E�̉����ɂ��� **[�ۑ�]** ���N���b�N���܂��B

    �f�v���C�ɂ͏������Ԃ�������ꍇ������܂��B

1. **[Set modules on device: turbine-06]** �u���[�h�̉����ɂ���A**[Review + create]** ���N���b�N���܂��B

1. **[Review + create]**�^�u�ŁA**Deployment Manifest** JSON���A�\�����ꂽ�΂���� Stream Analytics ���W���[���ƃ��[�e�B���O��`�ōX�V����Ă��邱�Ƃɒ��ڂ��Ă��������B

1. �u���[�h�̉����ɂ��� **[�쐬]** ���N���b�N���܂��B

1. Edge �p�b�P�[�W������Ɍ��J���ꂽ��A�V���� ASA ���W���[���� **[IoT Edge ���W���[��]** �Z�N�V�����̉��Ƀ��X�g����Ă��邱�Ƃɒ��ڂ��Ă��������B

1. **[IoT Edge ���W���[��]** �̉��ŁA**iotedge-streamjob-{deployment-id}** ���N���b�N���܂��B

    ����́AEdge �f�o�C�X�ɒǉ����ꂽ�΂���� Steam Analytics ���W���[���ł��B

1. **[Update IoT Edge Module]** �E�B���h�E�ŁA**[Image URI]** ���W���� Azure Stream Analytics �C���[�W���w���Ă��邱�Ƃɒ��ӂ��Ă��������B

    ```text
    mcr.microsoft.com/azure-stream-analytics/azureiotedge:1.0.7
    ```

    ����́AIoT Edge �f�o�C�X�Ƀf�v���C����邷�ׂĂ� ASA �W���u�Ɏg�p�����̂Ɠ����C���[�W�ł��B

    > **��**:  �\������Ă��� **[�C���[�W URI]** �̖����ɂ���o�[�W�����ԍ��́AStream Analytics ���W���[�����쐬�������_�ł̌��s�ŐV�o�[�W�����𔽉f���܂��B

1. ���ׂĂ̒l���f�t�H���g�̂܂܂ɂ��āA**[IoT Edge Custom Modules]** �E�B���h�E����܂��B

1. **[Set modules on device: turbine-06]**�E�B���h�E�ŁA**[Next: Routes >]** ���N���b�N���܂��B

    �����̃��[�e�B���O���\������Ă��邱�Ƃɒ��ӂ��Ă��������B

1. ��`����Ă������̃��[�g������ 3 �̃��[�g�ɒu�������܂��B
   
   > **��**: �K�� `iotstreamjob-edge-{deployment-id}` �v���[�X�z���_�[�� Azure Stream Analytics �W���u ���W���[���̖��O�ɒu�������Ă��������B
   
    * ���[�g 1
        * ���O: **telemetryToCloud**
        * �l: `FROM /messages/modules/turbinesensor/* INTO $upstream`
    * ���[�g 2
        * ���O: **alertsToReset**
        * �l: `/messages/modules/iotedge-streamjob-{deployment-id}/* ���� BrokeredEndpoint("/modules/turbinesensor/inputs/control")` ��
    * ���[�g 3
        * ���O: **telemetryToAsa**
        * �l: `/messages/modules/turbinesensor/* ���� BrokeredEndpoint("/modules/iotedge-streamjob-{deployment-id}/inputs/temperature")` ��

    > **��**: **[�O��]** ���N���b�N���ă��W���[���Ƃ��̖��O�̃��X�g��\�����A**[����]** ���N���b�N���Ă��̎菇�ɖ߂邱�Ƃ��ł��܂��B

    ��`����Ă��郋�[�g�͎��̂Ƃ���ł��B

    * **telemetryToCloud** ���[�g�́A`turbinesensor` ���W���[���o�͂���̂��ׂẴ��b�Z�[�W�� Azure IoT Hub �ɑ��M���܂��B
    * **alertsToReset** ���[�g�́AStream Analytics ���W���[���o�͂���̂��ׂẴA���[�g ���b�Z�[�W�� **turbinesensor** ���W���[���̓��͂ɑ��M���܂��B
    * **telemetryToAsa** ���[�g�́A`turbinesensor` ���W���[���o�͂���̂��ׂẴ��b�Z�[�W�� Stream Analytics ���W���[�����͂ɑ��M���܂��B

1. **[Set modules on device: turbine-06]** �u���[�h�̉����ɂ���A**[Review + create]** ���N���b�N���܂��B

1. **[Review + create]**�^�u�ŁA**Deployment Manifest** JSON���A�\�����ꂽ�΂���� Stream Analytics ���W���[���ƃ��[�e�B���O��`�ōX�V����Ă��邱�Ƃɒ��ڂ��Ă��������B

1. `turbinesensor` Simulated Temperature Sensor ���W���[���� JSON �\���ɒ��ڂ��Ă��������B

    ```json
    "turbinesensor": {
        "settings": {
            "image": "asaedgedockerhubtest/asa-edge-test-module:simulated-temperature-sensor",
            "createOptions": ""
        },
        "type": "docker",
        "version": "1.0",
        "status": "running",
        "restartPolicy": "always"
    },
    ```

1. �ȑO�ɍ\�����ꂽ���[�g�� JSON �\���ƁAJSON �f�v���C��`�ł���炪�ǂ̂悤�ɍ\������Ă��邩�ɒ��ڂ��Ă��������B

    ```json
    "$edgeHub": {
        "properties.desired": {
            "routes": {
                "telemetryToCloud": "FROM /messages/modules/turbinesensor/* INTO $upstream",
                "alertsToReset": "FROM /messages/modules/iotedge-streamjob-{deployment-id}/* INTO BrokeredEndpoint(\\\"/modules/turbinesensor/inputs/control\\\")",
                "telemetryToAsa": "FROM /messages/modules/turbinesensor/* INTO BrokeredEndpoint(\\\"/modules/iotedge-streamjob-{deployment-id}/inputs/temperature\\\")"
            },
            "schemaVersion": "1.0",
            "storeAndForwardConfiguration": {
                "timeToLiveSecs": 7200
            }
        }
    },
    ```

1. �u���[�h�̉����ɂ��� **[�쐬]** ���N���b�N���܂��B

#### �f�[�^������

1. **SSH** ����� **IoT Edge �f�o�C�X**�ɐڑ����Ă��� **Cloud Shell** �Z�b�V�����ɖ߂�܂��B  

    > **��**: �ڑ������Ă��邩�^�C���A�E�g�����ꍇ�́A�Đڑ����܂��B`SSH` �R�}���h�����s���A�O�Ɠ����悤�Ƀ��O�C�����܂��B

1. �R�}���h �v�����v�g�ŁA�f�o�C�X�Ƀf�v���C����Ă��郂�W���[���̃��X�g��\������ɂ́A���̃R�}���h����͂��܂��B

    ```cmd/sh
    iotedge list
    ```

    �V���� Stream Analytics ���W���[���� IoT Edge �f�o�C�X�ւ̃f�v���C�ɂ́A�����̎��Ԃ�������ꍇ������܂��B�W�J���ꂽ��A���̃R�}���h�ɂ���ďo�͂���郊�X�g�ɕ\������܂��B

    ```cmd/sh
    demouser@linuxagentvm-{deployment-id}:~$ iotedge list
    NAME                       STATUS           DESCRIPTION      CONFIG
    iotedge-streamjob-232539   running          Up a minute      mcr.microsoft.com/azure-stream-analytics/azureiotedge:1.0.5
    edgeAgent                  running          Up 6 hours       mcr.microsoft.com/azureiotedge-agent:1.0
    edgeHub                    running          Up 4 hours       mcr.microsoft.com/azureiotedge-hub:1.0
    turbinesensor              running          Up 4 hours       asaedgedockerhubtest/asa-edge-test-module:simulated-temperature-sensor
    ``` 

    > **��**:  Stream Analytics ���W���[�������X�g�ɕ\������Ȃ��ꍇ�́A1 �` 2 ���҂��Ă��������x�����Ă��������B���W���[���̃f�v���C�� IoT Edge �f�o�C�X�ōX�V�����ɂ́A�����̎��Ԃ�������ꍇ������܂��B

1. `turbinesensor` ���W���[���ɂ���� Edge �f�o�C�X���瑗�M�����e�����g�����Ď�����ɂ́A�R�}���h �v�����v�g�Ŏ��̃R�}���h����͂��܂��B

    ```cmd/sh
    iotedge logs turbinesensor
    ```

1. �������Ԃ�����ďo�͂��ώ@���܂��B
 
    ���̃C�x���g�̏o�͎͂��̂悤�ɂȂ�܂��B

    ```cmd/sh
    11/14/2019 22:26:44 - Send Json Event : {"machine":{"temperature":231.599999999999959,"pressure":1.0095600761599359},"ambient":{"temperature":21.430643635304012,"humidity":24},"timeCreated":"2019-11-14T22:26:44.7904425Z"}
    11/14/2019 22:26:45 - Send Json Event : {"machine":{"temperature":531.999999999999957,"pressure":1.0099208337508767},"ambient":{"temperature":20.569532965342297,"humidity":25},"timeCreated":"2019-11-14T22:26:45.2901801Z"}
    Received message
    Received message Body: [{"command":"reset"}]
    Received message MetaData: {"MessageId":null,"To":null,"ExpiryTimeUtc":"0001-01-01T00:00:00","CorrelationId":null,"SequenceNumber":0,"LockToken":"e0e778b5-60ff-4e5d-93a4-ba5295b995941","EnqueuedTimeUtc":"0001-01-01T00:00:00","DeliveryCount":0,"UserId":null,"MessageSchema":null,"CreationTimeUtc":"0001-01-01T00:00:00","ContentType":"application/json","InputName":"control","ConnectionDeviceId":"turbine-06","ConnectionModuleId":"vm-iot-edge-CP1119","ContentEncoding":"utf-8","Properties":{},"BodyStream":{"CanRead":true,"CanSeek":false,"CanWrite":false,"CanTimeout":false}}
    Resetting temperature sensor..
    11/14/2019 22:26:45 - Send Json Event : {"machine":{"temperature":320.4,"pressure":0.99945886361358849},"ambient":{"temperature":20.940019742324957,"humidity":26},"timeCreated":"2019-11-14T22:26:45.7931201Z"}
    ```
 
1. **turbinesensor** �ɂ���đ��M����鉷�x�e�����g�����Ď����Ă���Ƃ��ɁA`machine.temperature` �����ς� `72` �𒴂���ƁAStream Analytics �W���u�ɂ���� **reset** �R�}���h�����M����邱�Ƃɒ��ӂ��Ă��������B����́AStream Analytics �W���u �N�G���Őݒ肳�ꂽ�A�N�V�����ł��B

���̉��K�ł́AAzure IoT Edge �T�[�r�X�𗘗p���� Edge �f�o�C�X�Ń��b�Z�[�W���������܂����B
