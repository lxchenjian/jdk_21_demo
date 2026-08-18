# JDK 21 模块及包说明

> JDK 21 采用 JPMS（Java Platform Module System）模块化系统，核心类库以模块（module）形式组织，而非传统 jar 包。以下按模块分类，列出每个模块导出的公开包及其作用。

---

## java.base

JDK 的核心基础模块，定义了 Java 语言最基本的 API。

| 包名 | 作用 |
|---|---|
| java.io | 系统输入输出，包括文件读写、流操作、序列化等 |
| java.lang | Java 语言核心类，如 String、Math、Thread、System、Object 等 |
| java.lang.annotation | 注解相关核心类型，如 Annotation、ElementType、Retention 等 |
| java.lang.constant | 常量相关的 API，支持对常量进行建模和操作 |
| java.lang.foreign | 外部函数与内存 API（FFM API），用于调用本地代码和操作堆外内存 |
| java.lang.invoke | 动态语言支持，方法句柄（MethodHandle）、调用点（CallSite）等 |
| java.lang.module | 模块系统核心 API，模块描述符、模块层等 |
| java.lang.ref | 引用对象类，如 SoftReference、WeakReference、PhantomReference |
| java.lang.reflect | 反射 API，类、方法、字段、构造器的反射操作 |
| java.lang.runtime | 运行时相关 API，如 ScopedValue（作用域值，预览特性） |
| java.math | 大数运算，BigInteger 和 BigDecimal |
| java.net | 网络编程 API，Socket、ServerSocket、URL、URI、InetAddress 等 |
| java.net.spi | 网络相关的服务提供者接口（SPI） |
| java.nio | 缓冲区（Buffer）API，NIO 核心数据容器 |
| java.nio.channels | NIO 通道 API，如 FileChannel、SocketChannel、Selector 等 |
| java.nio.channels.spi | NIO 通道的服务提供者接口 |
| java.nio.charset | 字符集编解码 API，Charset、CharsetEncoder、CharsetDecoder |
| java.nio.charset.spi | 字符集的服务提供者接口 |
| java.nio.file | 文件系统 API，Path、Files、FileSystem 等（NIO.2） |
| java.nio.file.attribute | 文件属性相关 API，如 BasicFileAttributes、PosixFilePermissions |
| java.nio.file.spi | 文件系统的服务提供者接口 |
| java.security | 安全框架核心类，如 MessageDigest、Signature、KeyStore、SecureRandom |
| java.security.cert | 证书相关 API，如 X509Certificate、CertificateFactory、CertPath |
| java.security.interfaces | 密钥接口，如 RSAPublicKey、ECKey、DSAPrivateKey |
| java.security.spec | 密钥规范和算法参数规范，如 RSAPublicKeySpec、ECParameterSpec |
| java.text | 文本处理 API，如 DateFormat、NumberFormat、Collator、MessageFormat |
| java.text.spi | 文本处理的服务提供者接口 |
| java.time | 日期时间 API（JSR 310），如 LocalDate、LocalTime、ZonedDateTime、Instant |
| java.time.chrono | 日历系统 API，支持非 ISO 日历系统，如 HijrahChronology、JapaneseChronology |
| java.time.format | 日期时间格式化与解析 |
| java.time.temporal | 日期时间的时间域操作，如 TemporalField、TemporalAdjuster |
| java.time.zone | 时区相关 API，如 ZoneRules、ZoneOffsetTransition |
| java.util | 集合框架、日期（遗留）、随机数、扫描器、属性等工具类 |
| java.util.concurrent | 并发编程工具，如 ExecutorService、ConcurrentHashMap、CountDownLatch、CompletableFuture |
| java.util.concurrent.atomic | 原子变量类，如 AtomicInteger、AtomicReference、LongAdder |
| java.util.concurrent.locks | 锁框架，如 ReentrantLock、ReadWriteLock、StampedLock、Condition |
| java.util.function | 函数式接口，如 Function、Predicate、Consumer、Supplier、BiFunction |
| java.util.jar | JAR 文件读写 API，如 JarFile、JarOutputStream、Manifest |
| java.util.random | 随机数生成器 API，如 RandomGenerator、RandomGeneratorFactory |
| java.util.regex | 正则表达式 API，Pattern、Matcher |
| java.util.spi | 工具类的服务提供者接口 |
| java.util.stream | 流式编程 API，如 Stream、IntStream、Collector |
| java.util.zip | ZIP/GZIP 压缩与解压 API，如 ZipInputStream、GZIPOutputStream、Deflater |
| javax.crypto | 加密解密 API，如 Cipher、Mac、KeyGenerator |
| javax.crypto.interfaces | 加密密钥接口，如 DHPrivateKey、DHPublicKey |
| javax.crypto.spec | 加密密钥和参数规范，如 SecretKeySpec、IvParameterSpec、GCMParameterSpec |
| javax.net | 网络相关的安全套接字扩展基础类，如 SocketFactory、ServerSocketFactory |
| javax.net.ssl | SSL/TLS 安全套接字 API，如 SSLSocket、SSLServerSocket、SSLContext |
| javax.security.auth | 认证与授权框架核心类，如 Subject、LoginContext |
| javax.security.auth.callback | 认证回调交互 API，如 NameCallback、PasswordCallback |
| javax.security.auth.login | 登录配置和模块 API，如 Configuration、LoginModule |
| javax.security.auth.x500 | X500 主体相关 API，如 X500Principal |
| javax.security.cert | 已废弃的证书 API（建议使用 java.security.cert 替代） |

---

## java.compiler

Java 编译器 API，定义了注解处理和语言模型相关的 API。

| 包名 | 作用 |
|---|---|
| javax.annotation.processing | 注解处理框架 API，如 Processor、RoundEnvironment、Filer |
| javax.lang.model | 语言模型核心类型，如 SourceVersion、ElementKind |
| javax.lang.model.element | 语言模型元素，如 TypeElement、ExecutableElement、VariableElement |
| javax.lang.model.type | 语言模型类型，如 TypeMirror、DeclaredType、ArrayType |
| javax.lang.model.util | 语言模型工具类，如 Elements、Types、Scanner 系列 |
| javax.tools | 编译工具 API，如 JavaCompiler、ToolProvider、StandardJavaFileManager |

---

## java.datatransfer

数据传输模块，提供剪贴板和拖放数据传输支持。

| 包名 | 作用 |
|---|---|
| java.awt.datatransfer | 剪贴板和拖拽数据传输 API，如 Clipboard、Transferable、DataFlavor、StringSelection |

---

## java.desktop

桌面应用模块，包含 AWT、Swing、图像处理、打印、音频等 GUI 相关 API。

| 包名 | 作用 |
|---|---|
| java.applet | 已废弃的 Applet API（Applet 类已标记为废弃） |
| java.awt | AWT 核心类，如 Component、Container、Window、Frame、Graphics、Color、Font |
| java.awt.color | 颜色空间 API，如 ColorSpace、ICC_Profile |
| java.awt.desktop | 桌面集成 API，如 Desktop、AboutHandler、PreferencesHandler、ScreenSleepEvent |
| java.awt.dnd | 拖放（Drag and Drop）API，如 DragSource、DropTarget、Transferable |
| java.awt.event | AWT 事件模型，如 ActionListener、MouseEvent、KeyEvent、WindowEvent |
| java.awt.font | 字体相关 API，如 Font、TextLayout、LineMetrics、GlyphVector |
| java.awt.geom | 几何图形 API，如 Line2D、Rectangle2D、Ellipse2D、Path2D、AffineTransform |
| java.awt.im | 输入法框架 API，如 InputContext、InputMethodRequests |
| java.awt.im.spi | 输入法服务提供者接口 |
| java.awt.image | 图像处理 API，如 BufferedImage、ImageIO、ConvolveOp、RescaleOp |
| java.awt.image.renderable | 可渲染图像 API，如 RenderableImage、RenderableImageOp |
| java.awt.print | 打印 API，如 PrinterJob、PageFormat、Printable、Book |
| java.beans | JavaBeans 组件 API，如 BeanInfo、PropertyDescriptor、PropertyChangeListener |
| java.beans.beancontext | Bean 上下文 API，如 BeanContext、BeanContextServices |
| javax.accessibility | 无障碍辅助技术 API，如 Accessible、AccessibleContext、AccessibleRole |
| javax.imageio | 图像 I/O API，如 ImageReader、ImageWriter、ImageTranscoder |
| javax.imageio.event | 图像 I/O 事件 API，如 IIOReadProgressListener、IIOWriteProgressListener |
| javax.imageio.metadata | 图像 I/O 元数据 API，如 IIOMetadata、IIOMetadataFormat |
| javax.imageio.plugins.bmp | BMP 图像格式插件支持 |
| javax.imageio.plugins.jpeg | JPEG 图像格式插件支持 |
| javax.imageio.plugins.tiff | TIFF 图像格式插件支持 |
| javax.imageio.spi | 图像 I/O 服务提供者接口，如 ImageReaderSpi、ImageWriterSpi |
| javax.imageio.stream | 图像 I/O 流 API，如 ImageInputStream、ImageOutputStream |
| javax.print | 打印服务 API，如 PrintService、DocPrintJob、PrintServiceLookup |
| javax.print.attribute | 打印属性 API，如 PrintRequestAttributeSet、HashPrintAttributeSet |
| javax.print.attribute.standard | 标准打印属性，如 Copies、MediaSize、OrientationRequested、Sides |
| javax.print.event | 打印事件 API，如 PrintJobEvent、PrintServiceEvent |
| javax.sound.midi | MIDI 音频 API，如 Sequencer、Synthesizer、MidiSystem、Track |
| javax.sound.midi.spi | MIDI 服务提供者接口，如 MidiDeviceProvider、SoundbankReader |
| javax.sound.sampled | 采样音频 API，如 AudioSystem、Clip、SourceDataLine、AudioFormat |
| javax.sound.sampled.spi | 采样音频服务提供者接口，如 AudioFileReader、FormatConversionProvider |
| javax.swing | Swing 组件核心包，如 JFrame、JButton、JLabel、JPanel、JTextField、JTable |
| javax.swing.border | Swing 边框 API，如 Border、EtchedBorder、TitledBorder、LineBorder |
| javax.swing.colorchooser | Swing 颜色选择器 API，如 JColorChooser、AbstractColorChooserPanel |
| javax.swing.event | Swing 事件 API，如 ChangeEvent、ListSelectionEvent、HyperlinkEvent |
| javax.swing.filechooser | Swing 文件选择器 API，如 JFileChooser、FileFilter、FileSystemView |
| javax.swing.plaf | Swing 外观基础 API，如 ComponentUI、LookAndFeel、UIResource |
| javax.swing.plaf.basic | Swing 基础外观实现，如 BasicButtonUI、BasicScrollBarUI |
| javax.swing.plaf.metal | Metal 外观实现，如 MetalLookAndFeel、MetalButtonUI |
| javax.swing.plaf.multi | 多路外观实现，用于辅助技术支持 |
| javax.swing.plaf.nimbus | Nimbus 外观实现，如 NimbusLookAndFeel |
| javax.swing.plaf.synth | Synth 外观框架 API，如 SynthLookAndFeel、SynthStyle、SynthPainter |
| javax.swing.table | Swing 表格 API，如 JTable、TableModel、DefaultTableModel、TableColumn |
| javax.swing.text | Swing 文本组件 API，如 JTextComponent、JTextPane、Document、StyledDocument |
| javax.swing.text.html | HTML 文本组件支持，如 HTMLEditorKit、HTMLDocument |
| javax.swing.text.html.parser | HTML 解析器 API，如 Parser、DTD、TagElement |
| javax.swing.text.rtf | RTF 文本组件支持，如 RTFEditorKit |
| javax.swing.tree | Swing 树组件 API，如 JTree、TreeModel、DefaultMutableTreeNode、TreePath |
| javax.swing.undo | 撤销/重做 API，如 UndoManager、UndoableEdit、CompoundEdit |

---

## java.instrument

字节码插桩模块，提供 Java 代理（Agent）支持。

| 包名 | 作用 |
|---|---|
| java.lang.instrument | Java 代理 API，如 Instrumentation、ClassFileTransformer、ClassDefinition |

---

## java.logging

Java 日志模块。

| 包名 | 作用 |
|---|---|
| java.util.logging | Java 标准日志 API，如 Logger、LogManager、Handler、Formatter、Level |

---

## java.management

Java 管理扩展（JMX）核心模块。

| 包名 | 作用 |
|---|---|
| java.lang.management | JVM 监控管理 API，如 ManagementFactory、MemoryMXBean、ThreadMXBean、GarbageCollectorMXBean |
| javax.management | JMX 核心 API，如 MBeanServer、ObjectName、MBeanInfo、Query |
| javax.management.loading | JMX 动态类加载 API，如 MLet、MLetMBean |
| javax.management.modelmbean | 模型 MBean API，如 RequiredModelMBean、ModelMBeanInfo |
| javax.management.monitor | JMX 监视器 API，如 GaugeMonitor、CounterMonitor、StringMonitor |
| javax.management.openmbean | 开放类型 MBean API，如 CompositeType、TabularType、OpenMBeanInfo |
| javax.management.relation | JMX 关系服务 API，如 RelationType、Role、RelationService |
| javax.management.remote | JMX 远程管理 API，如 JMXConnector、JMXConnectorServer、JMXServiceURL |
| javax.management.timer | JMX 定时器 MBean API，如 TimerMBean、TimerNotification |

---

## java.management.rmi

JMX 远程管理的 RMI 传输模块。

| 包名 | 作用 |
|---|---|
| javax.management.remote.rmi | JMX RMI 连接器 API，如 RMIConnector、RMIConnectorServer、RMIServer |

---

## java.naming

JNDI（Java 命名与目录接口）模块。

| 包名 | 作用 |
|---|---|
| javax.naming | JNDI 命名服务核心 API，如 Context、InitialContext、Name、Binding |
| javax.naming.directory | JNDI 目录服务扩展 API，如 DirContext、SearchControls、Attributes |
| javax.naming.event | JNDI 事件通知 API，如 NamingEvent、EventDirContext、NamingListener |
| javax.naming.ldap | JNDI LDAP 扩展 API，如 LdapContext、StartTlsResponse、SortControl |
| javax.naming.ldap.spi | JNDI LDAP 服务提供者接口，如 LdapDnsProvider |
| javax.naming.spi | JNDI 服务提供者接口，如 InitialContextFactory、ObjectFactory、StateFactory |

---

## java.net.http

HTTP 客户端模块（JDK 11 引入，JDK 21 增强支持 HTTP/2 和 WebSocket）。

| 包名 | 作用 |
|---|---|
| java.net.http | 现代 HTTP 客户端 API，如 HttpClient、HttpRequest、HttpResponse、WebSocket |

---

## java.prefs

偏好设置（Preferences）模块。

| 包名 | 作用 |
|---|---|
| java.util.prefs | 用户/系统偏好设置 API，如 Preferences、PreferencesFactory、NodeChangeEvent |

---

## java.rmi

RMI（远程方法调用）模块。

| 包名 | 作用 |
|---|---|
| java.rmi | RMI 核心 API，如 Remote、UnicastRemoteObject、RemoteException、Naming |
| java.rmi.dgc | RMI 分布式垃圾回收 API，如 DGC、Lease、VMID |
| java.rmi.registry | RMI 注册表 API，如 Registry、LocateRegistry、RegistryHandler |
| java.rmi.server | RMI 服务端 API，如 RemoteServer、RemoteObject、RMISocketFactory、Unreferenced |
| javax.rmi.ssl | RMI 的 SSL 套接字工厂支持，如 SslRMIClientSocketFactory、SslRMIServerSocketFactory |

---

## java.scripting

脚本引擎模块（JSR 223）。

| 包名 | 作用 |
|---|---|
| javax.script | 脚本引擎 API，如 ScriptEngine、ScriptEngineManager、CompiledScript、Bindings |

---

## java.se

Java SE 平台聚合模块，不导出任何包，仅声明对其他模块的依赖以构成完整的 Java SE 平台。

> 该模块无导出包。

---

## java.security.jgss

GSS-API（通用安全服务 API）模块，支持 Kerberos 认证。

| 包名 | 作用 |
|---|---|
| javax.security.auth.kerberos | Kerberos 认证相关 API，如 KerberosTicket、KerberosPrincipal、KeyTab |
| org.ietf.jgss | GSS-API 绑定，如 GSSContext、GSSCredential、GSSName、MessageProp |

---

## java.security.sasl

SASL（简单认证与安全层）模块。

| 包名 | 作用 |
|---|---|
| javax.security.sasl | SASL 认证 API，如 SaslClient、SaslServer、SaslClientFactory、SaslServerFactory |

---

## java.smartcardio

智能卡 I/O 模块。

| 包名 | 作用 |
|---|---|
| javax.smartcardio | 智能卡通信 API，如 CardTerminal、CardChannel、CommandAPDU、TerminalFactory |

---

## java.sql

JDBC 核心 API 模块。

| 包名 | 作用 |
|---|---|
| java.sql | JDBC 核心 API，如 Connection、Statement、PreparedStatement、ResultSet、DriverManager、DataSource |
| javax.sql | JDBC 扩展 API，如 RowSet、ConnectionPoolDataSource、PooledConnection、ConnectionEvent |

---

## java.sql.rowset

JDBC RowSet 实现（RowSet 实现）模块。

| 包名 | 作用 |
|---|---|
| javax.sql.rowset | RowSet 实现 API，如 CachedRowSet、JdbcRowSet、WebRowSet、FilteredRowSet、JoinRowSet |
| javax.sql.rowset.serial | RowSet 序列化工具，如 SerialBlob、SerialClob、SerialArray、SerialJavaObject |
| javax.sql.rowset.spi | RowSet 服务提供者接口，如 SyncProvider、SyncFactory、XmlReader、XmlWriter |

---

## java.transaction.xa

分布式事务 XA 模块。

| 包名 | 作用 |
|---|---|
| javax.transaction.xa | XA 资源管理 API，如 XAResource、Xid、XAException |

---

## java.xml

JAXP（Java XML 处理 API）模块。

| 包名 | 作用 |
|---|---|
| javax.xml | XML 核心常量和通用类，如 XMLConstants |
| javax.xml.catalog | XML 目录 API，如 CatalogManager、CatalogResolver |
| javax.xml.datatype | XML/Java 数据类型映射 API，如 XMLGregorianCalendar、DatatypeFactory、Duration |
| javax.xml.namespace | XML 命名空间常量，如 QName |
| javax.xml.parsers | XML 解析 API，如 DocumentBuilderFactory、SAXParserFactory |
| javax.xml.stream | StAX 流式 XML API，如 XMLInputFactory、XMLOutputFactory、XMLEventReader |
| javax.xml.stream.events | StAX 事件接口，如 XMLEvent、StartElement、EndElement、Characters |
| javax.xml.stream.util | StAX 工具类，如 XMLEventAllocator、XMLEventConsumer |
| javax.xml.transform | XML 转换（XSLT）API，如 Transformer、TransformerFactory、Templates |
| javax.xml.transform.dom | DOM 转换源/结果，如 DOMSource、DOMResult |
| javax.xml.transform.sax | SAX 转换源/结果，如 SAXSource、SAXResult |
| javax.xml.transform.stax | StAX 转换源/结果，如 StAXSource、StAXResult |
| javax.xml.transform.stream | 流式转换源/结果，如 StreamSource、StreamResult |
| javax.xml.validation | XML 校验 API，如 SchemaFactory、Schema、Validator |
| javax.xml.xpath | XPath 查询 API，如 XPath、XPathFactory、XPathExpression |
| org.w3c.dom | W3C DOM 核心 API，如 Document、Node、Element、Attr、NodeList |
| org.w3c.dom.bootstrap | DOM 实现引导 API，如 DOMImplementationRegistry |
| org.w3c.dom.events | DOM 事件 API，如 Event、EventTarget、MouseEvent、DocumentEvent |
| org.w3c.dom.ls | DOM 加载与保存 API，如 LSParser、LSSerializer、LSInput、LSOutput |
| org.w3c.dom.ranges | DOM 范围 API，如 Range、RangeException |
| org.w3c.dom.traversal | DOM 遍历 API，如 NodeIterator、TreeWalker、NodeFilter |
| org.w3c.dom.views | DOM 视图 API，如 AbstractView、DocumentView |
| org.xml.sax | SAX XML 解析核心 API，如 XMLReader、ContentHandler、ErrorHandler、InputSource |
| org.xml.sax.ext | SAX 扩展接口，如 LexicalHandler、DeclHandler、Attributes2 |
| org.xml.sax.helpers | SAX 工具类，如 DefaultHandler、XMLReaderFactory、NamespaceSupport |

---

## java.xml.crypto

XML 签名与加密模块（JSR 105）。

| 包名 | 作用 |
|---|---|
| javax.xml.crypto | XML 加密通用 API，如 XMLStructure、AlgorithmMethod、KeySelector |
| javax.xml.crypto.dom | XML 加密的 DOM 实现，如 DOMStructure、DOMCryptoContext |
| javax.xml.crypto.dsig | XML 数字签名 API，如 XMLSignature、XMLSignatureFactory、SignedInfo |
| javax.xml.crypto.dsig.dom | XML 数字签名的 DOM 实现，如 DOMSignContext、DOMValidateContext |
| javax.xml.crypto.dsig.keyinfo | XML 签名密钥信息 API，如 KeyInfo、KeyInfoFactory、X509Data、RSAKeyValue |
| javax.xml.crypto.dsig.spec | XML 签名规范参数 API，如 SignatureMethodParameterSpec、HMACParameterSpec、XPathFilter2 |

---

## jdk.accessibility

辅助技术支持模块。

| 包名 | 作用 |
|---|---|
| com.sun.java.accessibility.util | 辅助技术工具类，如 AccessibilityEventMonitor、AccessibilityListenerList、Translator |

---

## jdk.attach

JVM 动态附加（Attach）模块。

| 包名 | 作用 |
|---|---|
| com.sun.tools.attach | JVM Attach API，如 VirtualMachine、AttachProvider、AttachNotSupportedException |
| com.sun.tools.attach.spi | Attach 服务提供者接口，如 AttachProvider |

---

## jdk.charsets

扩展字符集模块，提供 JDK 支持的额外字符编码。

> 该模块不导出公开包，通过 SPI 提供 `java.nio.charset.spi.CharsetProvider` 实现（如 ExtendedCharsets）。

---

## jdk.compiler

Java 编译器模块，包含 javac 编译器的实现和编译器树 API。

| 包名 | 作用 |
|---|---|
| com.sun.source.doctree | 文档树（DocTree）API，如 DocCommentTree、DocTree、SinceTree、AuthorTree |
| com.sun.source.tree | 编译器语法树（AST）API，如 CompilationUnitTree、MethodTree、ClassTree、ExpressionTree |
| com.sun.source.util | 编译器工具类，如 Trees、DocTrees、TreeScanner、JavacTask |

---

## jdk.crypto.cryptoki

PKCS#11 加密提供者模块。

> 该模块不导出公开包，通过 SPI 提供 `java.security.Provider` 实现（SunPKCS11），用于与 PKCS#11 加密硬件交互。

---

## jdk.crypto.ec

椭圆曲线加密提供者模块。

> 该模块不导出公开包，通过 SPI 提供 `java.security.Provider` 实现（SunEC），支持 ECDSA、ECDH 等椭圆曲线算法。

---

## jdk.dynalink

动态链接器模块，用于在 JVM 上实现动态语言的链接机制。

| 包名 | 作用 |
|---|---|
| jdk.dynalink | 动态链接器核心 API，如 DynamicLinker、DynamicLinkerFactory、CallSiteDescriptor |
| jdk.dynalink.beans | Java Bean 动态链接器，如 BeansLinker、BeanLinker |
| jdk.dynalink.linker | 链接器接口，如 GuardingDynamicLinker、GuardedInvocation、LinkerServices |
| jdk.dynalink.linker.support | 链接器支持工具类，如 TypeBasedGuardingDynamicLinker、GuardedInvocationTransformer |
| jdk.dynalink.support | 动态链接器辅助工具类 |

---

## jdk.editpad

JShell 内置编辑器模块。

> 该模块不导出公开包，提供 `jdk.internal.editor.spi.BuildInEditorProvider` 实现（EditPadProvider）。

---

## jdk.hotspot.agent

HotSpot 调试代理模块，用于调试和分析 JVM 状态。

> 该模块不导出公开包，内部使用。

---

## jdk.httpserver

轻量级 HTTP 服务器模块。

| 包名 | 作用 |
|---|---|
| com.sun.net.httpserver | HTTP 服务器 API，如 HttpServer、HttpHandler、HttpExchange、HttpContext |
| com.sun.net.httpserver.spi | HTTP 服务器服务提供者接口，如 HttpServerProvider |

---

## jdk.incubator.vector

向量计算 API（孵化器模块），支持 SIMD 向量运算。

| 包名 | 作用 |
|---|---|
| jdk.incubator.vector | 向量计算 API，如 Vector、IntVector、FloatVector、VectorSpecies、VectorMask |

---

## jdk.internal.ed

编辑器内部模块。

> 该模块不导出公开包，内部使用。

---

## jdk.internal.jvmstat

JVM 统计监控内部模块。

> 该模块不导出公开包，内部使用。

---

## jdk.internal.le

行编辑器（JLine）内部模块。

> 该模块不导出公开包，内部使用。

---

## jdk.internal.opt

命令行选项解析内部模块。

> 该模块不导出公开包，内部使用。

---

## jdk.internal.vm.ci

JVM 编译器接口（JVMCI）内部模块，用于 Graal 编译器集成。

> 该模块不导出公开包，内部使用。

---

## jdk.internal.vm.compiler

Graal JIT 编译器内部模块。

> 该模块不导出公开包，内部使用。

---

## jdk.internal.vm.compiler.management

Graal 编译器管理内部模块。

> 该模块不导出公开包，内部使用。

---

## jdk.jartool

JAR 工具模块，提供 jar 命令和 JAR 签名支持。

| 包名 | 作用 |
|---|---|
| jdk.security.jarsigner | JAR 签名 API，如 JarSigner、JarSigner.Builder |

---

## jdk.javadoc

Javadoc 文档生成工具模块。

| 包名 | 作用 |
|---|---|
| jdk.javadoc.doclet | Doclet API，如 Doclet、DocletEnvironment、Reporter、Taglet |

---

## jdk.jcmd

JVM 诊断命令（jcmd）模块。

> 该模块不导出公开包，提供 `jcmd`、`jps` 等诊断命令工具。

---

## jdk.jconsole

JConsole 监控工具模块。

| 包名 | 作用 |
|---|---|
| com.sun.tools.jconsole | JConsole 插件 API，如 JConsolePlugin、JConsoleContext |

---

## jdk.jdeps

类依赖分析工具模块，提供 `javap`、`jdeps` 命令。

> 该模块不导出公开包，提供字节码反编译和依赖分析工具。

---

## jdk.jdi

Java 调试接口（JDI）模块。

| 包名 | 作用 |
|---|---|
| com.sun.jdi | JDI 核心 API，如 VirtualMachine、ThreadReference、Type、Value、StackFrame |
| com.sun.jdi.connect | JDI 连接器 API，如 Connector、LaunchingConnector、AttachingConnector |
| com.sun.jdi.connect.spi | JDI 传输服务 API，如 TransportService、Connection |
| com.sun.jdi.event | JDI 事件 API，如 EventSet、BreakpointEvent、StepEvent、ClassPrepareEvent |
| com.sun.jdi.request | JDI 事件请求 API，如 EventRequestManager、BreakpointRequest、StepRequest |

---

## jdk.jdwp.agent

JDWP（Java 调试线协议）代理模块。

> 该模块不导出公开包，内部使用。

---

## jdk.jfr

JDK Flight Recorder（JFR）事件记录模块。

| 包名 | 作用 |
|---|---|
| jdk.jfr | JFR 事件定义 API，如 Event、EventFactory、Annotation（@Name、@Category、@Threshold） |
| jdk.jfr.consumer | JFR 事件消费 API，如 RecordingFile、EventStream、RecordedEvent、RecordedThread |

---

## jdk.jlink

JLink 模块链接工具模块，用于创建自定义运行时镜像。

> 该模块不导出公开包，提供 `jlink`、`jmod` 命令工具。

---

## jdk.jpackage

应用打包工具模块，用于将 Java 应用打包为原生安装包。

> 该模块不导出公开包，提供 `jpackage` 命令工具，支持生成 .dmg/.pkg（macOS）、.msi/.exe（Windows）、.deb/.rpm（Linux）安装包。

---

## jdk.jshell

JShell 交互式编程工具模块（Java REPL）。

| 包名 | 作用 |
|---|---|
| jdk.jshell | JShell API，如 JShell、Snippet、SnippetEvent、SourceCodeAnalysis |
| jdk.jshell.execution | JShell 执行引擎 API，如 LocalExecutionControl、JdiExecutionControl |
| jdk.jshell.spi | JShell 执行控制 SPI，如 ExecutionControl、ExecutionControlProvider |
| jdk.jshell.tool | JShell 命令行工具 API，如 JavaShellToolBuilder |

---

## jdk.jsobject

JavaScript 对象桥接模块。

| 包名 | 作用 |
|---|---|
| netscape.javascript | JSObject API，用于 Java 与 JavaScript 交互（如 JSObject、JSException） |

---

## jdk.jstatd

JVM 统计监控守护进程模块（jstatd）。

> 该模块不导出公开包，提供 `jstatd` 命令工具，用于远程 JVM 监控。

---

## jdk.localedata

本地化数据模块，提供各语言/地区的本地化资源。

> 该模块不导出公开包，通过 SPI 提供 LocaleData 资源（如 CLDR 数据、非基础地区数据）。

---

## jdk.management

JDK 扩展管理模块。

| 包名 | 作用 |
|---|---|
| com.sun.management | JDK 扩展管理 API，如 OperatingSystemMXBean、ThreadMXBean（扩展）、GarbageCollectorMXBean（扩展） |

---

## jdk.management.agent

JMX 管理代理模块。

> 该模块不导出公开包，提供 JMX 远程管理代理功能。

---

## jdk.management.jfr

JFR 管理模块，通过 JMX 管理 Flight Recorder。

| 包名 | 作用 |
|---|---|
| jdk.management.jfr | JFR 管理 API，如 FlightRecorderMXBean、RecordingInfo、EventTypeInfo、SettingControlInfo |

---

## jdk.naming.dns

DNS 命名提供者模块。

> 该模块不导出公开包，通过 SPI 提供 `javax.naming.spi.InitialContextFactory` 实现（DnsContextFactory），支持 JNDI DNS 查找。

---

## jdk.naming.rmi

RMI 命名提供者模块。

> 该模块不导出公开包，通过 SPI 提供 `javax.naming.spi.InitialContextFactory` 实现（RegistryContextFactory），支持通过 RMI 注册表进行 JNDI 查找。

---

## jdk.net

扩展网络功能模块。

| 包名 | 作用 |
|---|---|
| jdk.net | 扩展网络 API，如 Sockets、SocketFlow、ExtendedSocketOptions |
| jdk.nio | 扩展 NIO API，如 ExtendedNioOption |

---

## jdk.nio.mapmode

扩展 NIO 映射模式模块。

| 包名 | 作用 |
|---|---|
| jdk.nio.mapmode | 扩展文件映射模式，如 ExtendedMapMode（READ_ONLY_SYNC、READ_WRITE_SYNC） |

---

## jdk.random

扩展随机数生成器模块。

> 该模块不导出公开包，通过 SPI 提供多种随机数算法实现，如 L32X64MixRandom、L64X128MixRandom、Xoroshiro128PlusPlus、Xoshiro256PlusPlus 等。

---

## jdk.sctp

SCTP（流控制传输协议）模块。

| 包名 | 作用 |
|---|---|
| com.sun.nio.sctp | SCTP 通信 API，如 SctpChannel、SctpServerChannel、SctpMultiChannel、MessageInfo、Association |

---

## jdk.security.auth

扩展安全认证模块。

| 包名 | 作用 |
|---|---|
| com.sun.security.auth | 认证主体类，如 LdapPrincipal、UnixPrincipal、NTUserPrincipal、UserPrincipal |
| com.sun.security.auth.callback | 认证回调实现，如 TextCallbackHandler |
| com.sun.security.auth.login | 登录配置实现，如 ConfigFile |
| com.sun.security.auth.module | 登录模块实现，如 Krb5LoginModule、UnixLoginModule、LdapLoginModule、KeyStoreLoginModule |

---

## jdk.security.jgss

扩展 GSS-API 安全模块。

| 包名 | 作用 |
|---|---|
| com.sun.security.jgss | 扩展 GSS-API 凭据授权 API，如 ExtendedGSSContext、ExtendedGSSCredential、InquireType |

---

## jdk.unsupported

不支持/非标准 API 模块，包含内部 API 的公开入口。

| 包名 | 作用 |
|---|---|
| com.sun.nio.file | 扩展文件系统 API，如 ExtendedWatchEventModifier、SensitivityWatchEventModifier |
| sun.misc | 非标准内部 API，如 Signal、SignalHandler、Unsafe（已废弃，建议使用 jdk.internal.misc） |
| sun.reflect | 非标准反射 API，如 Reflection、ReflectionFactory |

---

## jdk.unsupported.desktop

不支持/非标准桌面 API 模块。

| 包名 | 作用 |
|---|---|
| jdk.swing.interop | Swing 互操作 API，如 InteropProvider、SwingInteroperabilityUtils |

---

## jdk.xml.dom

扩展 DOM API 模块，提供 W3C DOM 规范中可选部分的实现。

| 包名 | 作用 |
|---|---|
| org.w3c.dom.css | DOM CSS API，如 CSSStyleDeclaration、CSSStyleSheet、CSSRule、CSSStyleRule |
| org.w3c.dom.html | DOM HTML API，如 HTMLDocument、HTMLElement、HTMLBodyElement、HTMLFormElement |
| org.w3c.dom.stylesheets | DOM 样式表 API，如 StyleSheet、StyleSheetList、MediaList |
| org.w3c.dom.xpath | DOM XPath API，如 XPathEvaluator、XPathExpression、XPathResult、XPathNSResolver |

---

## jdk.zipfs

ZIP 文件系统模块。

> 该模块不导出公开包，通过 SPI 提供 `java.nio.file.spi.FileSystemProvider` 实现（ZipFileSystemProvider），支持将 ZIP/JAR 文件作为文件系统访问。
