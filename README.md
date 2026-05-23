Nome: AK47
Classe: Tool
Path: Players.rip_cria6177.Backpack.AK47
Parent: Backpack
Archivable: true

    Nome: HookJoints
    Classe: Script
    Path: Players.rip_cria6177.Backpack.AK47.HookJoints
    Parent: AK47
    Archivable: true
    >>> SCRIPT ENCONTRADO <<<
    Source:
    

    Nome: Cfg
    Classe: ModuleScript
    Path: Players.rip_cria6177.Backpack.AK47.Cfg
    Parent: AK47
    Archivable: true
    >>> SCRIPT ENCONTRADO <<<
    Source:
    

    Nome: OrpheusGunServer
    Classe: Script
    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunServer
    Parent: AK47
    Archivable: true
    >>> SCRIPT ENCONTRADO <<<
    Source:
    

        Nome: InflictTarget
        Classe: RemoteEvent
        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunServer.InflictTarget
        Parent: OrpheusGunServer
        Archivable: true
        >>> REMOTE ENCONTRADO <<<

        Nome: AtualizaMuniRemote
        Classe: RemoteEvent
        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunServer.AtualizaMuniRemote
        Parent: OrpheusGunServer
        Archivable: true
        >>> REMOTE ENCONTRADO <<<

        Nome: Mag
        Classe: NumberValue
        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunServer.Mag
        Parent: OrpheusGunServer
        Archivable: true
        Value: 30

        Nome: Ammo
        Classe: NumberValue
        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunServer.Ammo
        Parent: OrpheusGunServer
        Archivable: true
        Value: 0

    Nome: OrpheusGunClient
    Classe: LocalScript
    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient
    Parent: AK47
    Archivable: true
    >>> SCRIPT ENCONTRADO <<<
    Source:
    

        Nome: CFGSetup
        Classe: LocalScript
        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.CFGSetup
        Parent: OrpheusGunClient
        Archivable: true
        >>> SCRIPT ENCONTRADO <<<
        Source:
        

            Nome: Tipo
            Classe: StringValue
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.CFGSetup.Tipo
            Parent: CFGSetup
            Archivable: true
            Value: Fuzil

        Nome: AnimSys
        Classe: LocalScript
        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.AnimSys
        Parent: OrpheusGunClient
        Archivable: true
        >>> SCRIPT ENCONTRADO <<<
        Source:
        

            Nome: SacarSom
            Classe: Sound
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.AnimSys.SacarSom
            Parent: AnimSys
            Archivable: true

            Nome: SacarAnim
            Classe: Animation
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.AnimSys.SacarAnim
            Parent: AnimSys
            Archivable: true

        Nome: RollSys
        Classe: LocalScript
        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys
        Parent: OrpheusGunClient
        Archivable: true
        >>> SCRIPT ENCONTRADO <<<
        Source:
        

            Nome: RolasSom
            Classe: Sound
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys.RolasSom
            Parent: RollSys
            Archivable: true

            Nome: VinhetaGui
            Classe: ScreenGui
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys.VinhetaGui
            Parent: RollSys
            Archivable: true

                Nome: ScopeFrame
                Classe: Frame
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys.VinhetaGui.ScopeFrame
                Parent: VinhetaGui
                Archivable: true

                    Nome: ScopeImage
                    Classe: ImageLabel
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys.VinhetaGui.ScopeFrame.ScopeImage
                    Parent: ScopeFrame
                    Archivable: true

                        Nome: LeftBlack
                        Classe: Frame
                        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys.VinhetaGui.ScopeFrame.ScopeImage.LeftBlack
                        Parent: ScopeImage
                        Archivable: true

                        Nome: RightBlack
                        Classe: Frame
                        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys.VinhetaGui.ScopeFrame.ScopeImage.RightBlack
                        Parent: ScopeImage
                        Archivable: true

                        Nome: BottomBlack
                        Classe: Frame
                        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys.VinhetaGui.ScopeFrame.ScopeImage.BottomBlack
                        Parent: ScopeImage
                        Archivable: true

                        Nome: TopBlack
                        Classe: Frame
                        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys.VinhetaGui.ScopeFrame.ScopeImage.TopBlack
                        Parent: ScopeImage
                        Archivable: true

                        Nome: UIAspectRatioConstraint
                        Classe: UIAspectRatioConstraint
                        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys.VinhetaGui.ScopeFrame.ScopeImage.UIAspectRatioConstraint
                        Parent: ScopeImage
                        Archivable: true

                    Nome: UIListLayout
                    Classe: UIListLayout
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys.VinhetaGui.ScopeFrame.UIListLayout
                    Parent: ScopeFrame
                    Archivable: true

                Nome: Vinheta
                Classe: ImageLabel
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.RollSys.VinhetaGui.Vinheta
                Parent: VinhetaGui
                Archivable: true

        Nome: GunGUI
        Classe: ScreenGui
        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI
        Parent: OrpheusGunClient
        Archivable: true

            Nome: Crosshair
            Classe: Frame
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Crosshair
            Parent: GunGUI
            Archivable: true

                Nome: MarkerSound
                Classe: Sound
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Crosshair.MarkerSound
                Parent: Crosshair
                Archivable: true

                Nome: Hitmarker
                Classe: ImageLabel
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Crosshair.Hitmarker
                Parent: Crosshair
                Archivable: true

                Nome: HitMarkerPos
                Classe: TextLabel
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Crosshair.HitMarkerPos
                Parent: Crosshair
                Archivable: true

                Nome: UIListLayout
                Classe: UIListLayout
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Crosshair.UIListLayout
                Parent: Crosshair
                Archivable: true

            Nome: MobileButtons
            Classe: Frame
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.MobileButtons
            Parent: GunGUI
            Archivable: true

                Nome: ReloadButton
                Classe: ImageButton
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.MobileButtons.ReloadButton
                Parent: MobileButtons
                Archivable: true

                Nome: HoldDownButton
                Classe: ImageButton
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.MobileButtons.HoldDownButton
                Parent: MobileButtons
                Archivable: true

                Nome: AimButton
                Classe: ImageButton
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.MobileButtons.AimButton
                Parent: MobileButtons
                Archivable: true

                Nome: AimButton2
                Classe: ImageButton
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.MobileButtons.AimButton2
                Parent: MobileButtons
                Archivable: true

                Nome: ChangePosButton
                Classe: ImageButton
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.MobileButtons.ChangePosButton
                Parent: MobileButtons
                Archivable: true

                Nome: RolasButton
                Classe: ImageButton
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.MobileButtons.RolasButton
                Parent: MobileButtons
                Archivable: true

                Nome: CrosshairMobile
                Classe: Frame
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.MobileButtons.CrosshairMobile
                Parent: MobileButtons
                Archivable: true

                    Nome: UICorner
                    Classe: UICorner
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.MobileButtons.CrosshairMobile.UICorner
                    Parent: CrosshairMobile
                    Archivable: true

                    Nome: UIStroke
                    Classe: UIStroke
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.MobileButtons.CrosshairMobile.UIStroke
                    Parent: CrosshairMobile
                    Archivable: true

            Nome: Scope
            Classe: Frame
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Scope
            Parent: GunGUI
            Archivable: true

                Nome: ZoomSound
                Classe: Sound
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Scope.ZoomSound
                Parent: Scope
                Archivable: true

                Nome: Main
                Classe: Frame
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Scope.Main
                Parent: Scope
                Archivable: true

                    Nome: ScopeImg2
                    Classe: ImageLabel
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Scope.Main.ScopeImg2
                    Parent: Main
                    Archivable: true

                    Nome: ScopeImg1
                    Classe: ImageLabel
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Scope.Main.ScopeImg1
                    Parent: Main
                    Archivable: true

                    Nome: F2
                    Classe: Frame
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Scope.Main.F2
                    Parent: Main
                    Archivable: true

                    Nome: F1
                    Classe: Frame
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Scope.Main.F1
                    Parent: Main
                    Archivable: true

            Nome: Frame
            Classe: Frame
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Frame
            Parent: GunGUI
            Archivable: true

                Nome: Mag
                Classe: Frame
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Frame.Mag
                Parent: Frame
                Archivable: true

                    Nome: Current
                    Classe: TextLabel
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Frame.Mag.Current
                    Parent: Mag
                    Archivable: true

                        Nome: Max
                        Classe: TextLabel
                        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Frame.Mag.Current.Max
                        Parent: Current
                        Archivable: true

                        Nome: UIStroke
                        Classe: UIStroke
                        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Frame.Mag.Current.UIStroke
                        Parent: Current
                        Archivable: true

                    Nome: Arma
                    Classe: TextLabel
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Frame.Mag.Arma
                    Parent: Mag
                    Archivable: true

                        Nome: UIStroke
                        Classe: UIStroke
                        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Frame.Mag.Arma.UIStroke
                        Parent: Arma
                        Archivable: true

                    Nome: Reloading
                    Classe: TextLabel
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Frame.Mag.Reloading
                    Parent: Mag
                    Archivable: true

                    Nome: UIListLayout
                    Classe: UIListLayout
                    Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.GunGUI.Frame.Mag.UIListLayout
                    Parent: Mag
                    Archivable: true

        Nome: BloodEffect
        Classe: Folder
        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.BloodEffect
        Parent: OrpheusGunClient
        Archivable: true

            Nome: Blood
            Classe: ParticleEmitter
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.BloodEffect.Blood
            Parent: BloodEffect
            Archivable: true

                Nome: EmitCount
                Classe: IntValue
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.BloodEffect.Blood.EmitCount
                Parent: Blood
                Archivable: true
                Value: 3

        Nome: HitEffect
        Classe: Folder
        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.HitEffect
        Parent: OrpheusGunClient
        Archivable: true

            Nome: Spark
            Classe: ParticleEmitter
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.HitEffect.Spark
            Parent: HitEffect
            Archivable: true

                Nome: EmitCount
                Classe: IntValue
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.HitEffect.Spark.EmitCount
                Parent: Spark
                Archivable: true
                Value: 3

            Nome: Smoke
            Classe: ParticleEmitter
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.HitEffect.Smoke
            Parent: HitEffect
            Archivable: true
            Atributos:
              EmitCount = 3

                Nome: EmitCount
                Classe: IntValue
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.HitEffect.Smoke.EmitCount
                Parent: Smoke
                Archivable: true
                Value: 3

            Nome: Muzzle
            Classe: ParticleEmitter
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.HitEffect.Muzzle
            Parent: HitEffect
            Archivable: true
            Atributos:
              EmitCount = 8

                Nome: EmitCount
                Classe: IntValue
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.HitEffect.Muzzle.EmitCount
                Parent: Muzzle
                Archivable: true
                Value: 1

        Nome: MuzzleEffect
        Classe: Folder
        Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.MuzzleEffect
        Parent: OrpheusGunClient
        Archivable: true

            Nome: Spark
            Classe: ParticleEmitter
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.MuzzleEffect.Spark
            Parent: MuzzleEffect
            Archivable: true
            Atributos:
              EmitCount = 1

                Nome: EmitCount
                Classe: IntValue
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.MuzzleEffect.Spark.EmitCount
                Parent: Spark
                Archivable: true
                Value: 4

            Nome: Smoke
            Classe: ParticleEmitter
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.MuzzleEffect.Smoke
            Parent: MuzzleEffect
            Archivable: true
            Atributos:
              EmitDelay = 0.1
              EmitCount = 4
              EmitDuration = 0.3

                Nome: EmitCount
                Classe: IntValue
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.MuzzleEffect.Smoke.EmitCount
                Parent: Smoke
                Archivable: true
                Value: 4

            Nome: Muzzle2
            Classe: ParticleEmitter
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.MuzzleEffect.Muzzle2
            Parent: MuzzleEffect
            Archivable: true
            Atributos:
              EmitDelay = 0
              EmitCount = 1

                Nome: EmitCount
                Classe: IntValue
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.MuzzleEffect.Muzzle2.EmitCount
                Parent: Muzzle2
                Archivable: true
                Value: 3

            Nome: Muzzle
            Classe: ParticleEmitter
            Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.MuzzleEffect.Muzzle
            Parent: MuzzleEffect
            Archivable: true
            Atributos:
              EmitDelay = 0
              EmitCount = 1

                Nome: EmitCount
                Classe: IntValue
                Path: Players.rip_cria6177.Backpack.AK47.OrpheusGunClient.MuzzleEffect.Muzzle.EmitCount
                Parent: Muzzle
                Archivable: true
                Value: 3

    Nome: AK
    Classe: Model
    Path: Players.rip_cria6177.Backpack.AK47.AK
    Parent: AK47
    Archivable: true

        Nome: ak47.077
        Classe: MeshPart
        Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.077
        Parent: AK
        Archivable: true

            Nome: qCFrameWeldThingy
            Classe: Weld
            Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.077.qCFrameWeldThingy
            Parent: ak47.077
            Archivable: true

            Nome: qRelativeCFrameWeldValue
            Classe: CFrameValue
            Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.077.qRelativeCFrameWeldValue
            Parent: ak47.077
            Archivable: true
            Value: -0.564483643, -0.367477417, -0.0150146484, -0.0758693218, 0.0479343981, -0.995964885, 0.0035888534, 0.998850465, 0.0477998853, 0.99711132, 5.2170828e-05, -0.0759540796

        Nome: ak47.018
        Classe: MeshPart
        Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.018
        Parent: AK
        Archivable: true

            Nome: qCFrameWeldThingy
            Classe: Weld
            Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.018.qCFrameWeldThingy
            Parent: ak47.018
            Archivable: true

            Nome: qRelativeCFrameWeldValue
            Classe: CFrameValue
            Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.018.qRelativeCFrameWeldValue
            Parent: ak47.018
            Archivable: true
            Value: -0.0301513672, -0.707107544, 0.116455078, -0.0758693218, 0.0479343981, -0.995964885, 0.0035888534, 0.998850465, 0.0477998853, 0.99711132, 5.2170828e-05, -0.0759540796

        Nome: ak47.043
        Classe: MeshPart
        Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.043
        Parent: AK
        Archivable: true

            Nome: qCFrameWeldThingy
            Classe: Weld
            Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.043.qCFrameWeldThingy
            Parent: ak47.043
            Archivable: true

            Nome: qRelativeCFrameWeldValue
            Classe: CFrameValue
            Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.043.qRelativeCFrameWeldValue
            Parent: ak47.043
            Archivable: true
            Value: -0.264373779, -0.627807617, -0.0113525391, -0.0758693218, 0.0479343981, -0.995964885, 0.0035888534, 0.998850465, 0.0477998853, 0.99711132, 5.2170828e-05, -0.0759540796

        Nome: ak47.035
        Classe: MeshPart
        Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.035
        Parent: AK
        Archivable: true

            Nome: qCFrameWeldThingy
            Classe: Weld
            Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.035.qCFrameWeldThingy
            Parent: ak47.035
            Archivable: true

            Nome: qRelativeCFrameWeldValue
            Classe: CFrameValue
            Path: Players.rip_cria6177.Backpack.AK47.AK.ak47.035.qRelativeCFrameWeldValue
            Parent: ak47.035
            Archivable: true
            Value: 0.889221191, -0.644958496, 0.0823974609, -0.0758693218, 0.0479343981, -0.995964885, 0.0035888534, 0.998850465, 0.0477998853, 0.99711132, 5.2170828e-05, -0.0759540796

    Nome: IdleAnim
    Classe: Animation
    Path: Players.rip_cria6177.Backpack.AK47.IdleAnim
    Parent: AK47
    Archivable: true

    Nome: FireAnim
    Classe: Animation
    Path: Players.rip_cria6177.Backpack.AK47.FireAnim
    Parent: AK47
    Archivable: true

    Nome: ReloadAnim
    Classe: Animation
    Path: Players.rip_cria6177.Backpack.AK47.ReloadAnim
    Parent: AK47
    Archivable: true

    Nome: AimAnim
    Classe: Animation
    Path: Players.rip_cria6177.Backpack.AK47.AimAnim
    Parent: AK47
    Archivable: true

    Nome: Handle
    Classe: Part
    Path: Players.rip_cria6177.Backpack.AK47.Handle
    Parent: AK47
    Archivable: true

        Nome: ChargeSound
        Classe: Sound
        Path: Players.rip_cria6177.Backpack.AK47.Handle.ChargeSound
        Parent: Handle
        Archivable: true

        Nome: EmptyMag
        Classe: Sound
        Path: Players.rip_cria6177.Backpack.AK47.Handle.EmptyMag
        Parent: Handle
        Archivable: true

        Nome: EquippedSound
        Classe: Sound
        Path: Players.rip_cria6177.Backpack.AK47.Handle.EquippedSound
        Parent: Handle
        Archivable: true

        Nome: ShotgunClipin
        Classe: Sound
        Path: Players.rip_cria6177.Backpack.AK47.Handle.ShotgunClipin
        Parent: Handle
        Archivable: true

        Nome: WindDown
        Classe: Sound
        Path: Players.rip_cria6177.Backpack.AK47.Handle.WindDown
        Parent: Handle
        Archivable: true

        Nome: WindUp
        Classe: Sound
        Path: Players.rip_cria6177.Backpack.AK47.Handle.WindUp
        Parent: Handle
        Archivable: true

        Nome: ReloadSound
        Classe: Sound
        Path: Players.rip_cria6177.Backpack.AK47.Handle.ReloadSound
        Parent: Handle
        Archivable: true

        Nome: FireSound
        Classe: Sound
        Path: Players.rip_cria6177.Backpack.AK47.Handle.FireSound
        Parent: Handle
        Archivable: true

        Nome: MiraSound
        Classe: Sound
        Path: Players.rip_cria6177.Backpack.AK47.Handle.MiraSound
        Parent: Handle
        Archivable: true

    Nome: AttachSilenciador
    Classe: MeshPart
    Path: Players.rip_cria6177.Backpack.AK47.AttachSilenciador
    Parent: AK47
    Archivable: true

        Nome: qCFrameWeldThingy
        Classe: Weld
        Path: Players.rip_cria6177.Backpack.AK47.AttachSilenciador.qCFrameWeldThingy
        Parent: AttachSilenciador
        Archivable: true

        Nome: qRelativeCFrameWeldValue
        Classe: CFrameValue
        Path: Players.rip_cria6177.Backpack.AK47.AttachSilenciador.qRelativeCFrameWeldValue
        Parent: AttachSilenciador
        Archivable: true
        Value: -0.0722045898, -0.627807617, 3.22610474, -0.999993443, 0.00362543506, 8.97644204e-05, 0.00362559897, 0.999991596, 0.00189892389, -8.28792399e-05, 0.00189923681, -0.999998212

    Nome: Mag
    Classe: MeshPart
    Path: Players.rip_cria6177.Backpack.AK47.Mag
    Parent: AK47
    Archivable: true

        Nome: qCFrameWeldThingy
        Classe: Weld
        Path: Players.rip_cria6177.Backpack.AK47.Mag.qCFrameWeldThingy
        Parent: Mag
        Archivable: true

        Nome: qRelativeCFrameWeldValue
        Classe: CFrameValue
        Path: Players.rip_cria6177.Backpack.AK47.Mag.qRelativeCFrameWeldValue
        Parent: Mag
        Archivable: true
        Value: 0.0323791504, -0.0250244141, 0.0201416016, -0.0758693218, 0.0479343981, -0.995964885, 0.0035888534, 0.998850465, 0.0477998853, 0.99711132, 5.2170828e-05, -0.0759540796
