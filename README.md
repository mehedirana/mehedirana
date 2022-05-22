# Hi I am Md.Mehedi Rana Shuvo 👋

- 🔭 I’m currently working  as a Software Engineer
- 🌱 I’m currently learning Golang
- 👯 I’m looking to collaborate opensource
- 🤔 I’m looking for help with ...
- 💬 Ask me about React, React Native or Any Tech Related or JS
- 📫 How to reach me:  LinkedIn - https://www.linkedin.com/in/mehedi-rana-shuvo-653969173/
 

- 😄 Pronouns: He/they
- ⚡ Fun fact: ...

 ![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=mehedirana&show_icons=true&theme=tokyonight)
 [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=mehedirana&theme=tokyonight&layout=compact)](https://github.com/anuraghazra/github-readme-stats)

 ## Languages , Frameworks and Tools
<img align="left" alt="js" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
<img align="left" alt="react" src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"/>
<img align="left" alt="react" src="https://img.shields.io/badge/-React%20Native-black"/>
<code><img height="40" src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/8e/Nextjs-logo.svg/1200px-Nextjs-logo.svg.png"></code>
<img align="left" alt="redux" src="https://img.shields.io/badge/Redux-593D88?style=for-the-badge&logo=redux&logoColor=white"/>
<img align="left" alt="html5" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
<img alt="json" src="https://img.shields.io/badge/json-5E5C5C?style=for-the-badge&logo=json&logoColor=white"/>
<img alt="c" src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white" />
<code><img height="40" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/cpp/cpp.png"></code>
<code><img height="40" src="https://www.edureka.co/blog/wp-content/uploads/2019/07/express-logo.png"></code>
<img alt="node" src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white"/>
<code><img height="40" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/git/git.png"></code>
<img align="left" alt="bootstrap" src="https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white"/>
<img alt="material-ui" src="https://img.shields.io/badge/Material--UI-0081CB?style=for-the-badge&logo=material-ui&logoColor=white"/>
<img alt="npm" src="https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white"/>
<img alt="jira" src="https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=Jira&logoColor=white"/>
<img align="left" alt="firebase" src="https://img.shields.io/badge/firebase-ffca28?style=for-the-badge&logo=firebase&logoColor=black"/>
<img align="left" alt="mongo" src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white"/>
<img alt="mysql" src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white"/>
<code><img height="40" src="https://user-images.githubusercontent.com/39426829/142417748-88d64955-8403-4ebd-a555-2f67bd62eec2.png"></code>
<code><img height="40" src="https://mir-s3-cdn-cf.behance.net/project_modules/disp/a9326d72465217.5be8ae1c0a8a7.png"></code>
<code><img height="40" src="https://upload.wikimedia.org/wikipedia/en/0/0c/Xcode_icon.png"></code>




### Contact Me <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="25px">

<a href="https://www.linkedin.com/in/mehedi-rana-shuvo-653969173/">
  <img align="left" alt="Abhishek's LinkedIN" width="22px" src="https://raw.githubusercontent.com/peterthehan/peterthehan/master/assets/linkedin.svg" />
</a>


![](https://visitor-badge.glitch.me/badge?page_id=mehedirana)

<br />

### How this works
This is autogenerated by a Ruby script that runs on Actions. [See it here](https://github.com/mscoutermarsh/mscoutermarsh).


![](https://github.com/mscoutermarsh/mscoutermarsh/blob/master/teeter.gif?raw=true)



import React, { useEffect, useState } from 'react';
import { useTranslation } from 'react-i18next';
import {
  Image,
  SafeAreaView,
  StyleSheet,
  Text,
  TextInput,
  TouchableOpacity,
  View,
  ScrollView
} from 'react-native';
import { useDispatch } from 'react-redux';
import {
  ButtonArrow,
  ContainerBackgroundImage,
  HeaderNavigation,
  HeaderOnBoard,
} from '../../components/input';
import Message from '../../components/ToastMessage';
import { COLORS, FONTS } from '../../constants';
import { registrationEmailOne, emailAvailability } from '../../services/account/account';
import { userLogIn } from '../../store/auth/userAction';
import NetInfo from "@react-native-community/netinfo";
import LeftArrow from '../../assets/images/svg/LeftArrow';

const RegistrationWithEmail = ({ navigation }) => {
  const { t, i18n } = useTranslation();
  const [value, setValue] = useState('');
  const [name, setName] = useState('')
  const [pin, setPin] = useState('')
  const [isAvailable, setIsAvailable] = useState(false)
  const [isEmailUnfocus, setIsEmailUnfocus] = useState(true);
  const [sms, setSms] = useState('');
  const [color, setColor] = useState('red');
  const [messages, setMessages] = useState('');
  const [isLoading, setIsLoading] = useState(false);
  const [secureEntry, setSecureEntry] = useState(true)

  const dispatch = useDispatch()

  // useEffect(() => {
  //   if (phoneNumber === '1234') {
  //     dispatch(userLogIn({ phoneNumber, name: 'mehedi' }))
  //   }
  // }, [phoneNumber])

  const regiWithEmail = () => {
    NetInfo.fetch().then(async state => {
      if (state.isConnected) {
        console.log(value)
        const body = {
          email: value,
          step: 1,
          resend: false
        }
        const bodyTwo = {
          email: value,
          fullname: name,
          password: pin,
          step: 2
        }
        registrationEmailOne(body).then(res => {
          console.log(res)
          setIsLoading(true)
          if (res?.success) {
            setIsLoading(false)
            navigation.navigate('VerifyOTPScreen', {
              payload: res,
              data: bodyTwo
            });
          } else {
            console.log('error', res)
            setMessages(res?.error_message);
            setIsLoading(false)
          }
        }).catch(e => {
          console.log('error', e);
          setIsLoading(false)
        })
      } else {
        setMessages("You're currently offline. Please check internet")
      }
    });
  };

  const checkEmail = () => {
    NetInfo.fetch().then(async state => {
      if (state.isConnected) {
        // let reg = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w\w+)+$/;
        // if (reg.test(text) === false) {
        //   console.log("Email is Not Correct");
        //   setSms("Email is Not Correct")
        //   setColor('red')
        //   setIsAvailable(false);
        // }
        // else {
        // setValue(text.trim());
        emailAvailability(value).then(res => {
          if (res?.success) {
            if (res?.data?.available) {
              // setIsAvailable(true);
              regiWithEmail();

            } else {
              setIsAvailable(false);
              setMessages('Email is not available!');
            }
          } else {
            setIsAvailable(false)
          }
        }).catch(e => console.log(e))

        // }
      } else {
        setMessages("You're currently offline. Please check internet")
      }
    });
  }

  return (
    <View style={styles.container}>
      {messages != '' && (
        <Message
          message={messages}
          color={COLORS.red}
          onHide={() => {
            setMessages('');
          }}
        />
      )}
      <ContainerBackgroundImage imageSelect={1}>
        <ScrollView>
          <TouchableOpacity style={{ marginLeft: -5 }} onPress={() => navigation.goBack()}>
            <LeftArrow />
          </TouchableOpacity>
          <View style={styles.contentText}>
            <Text style={[styles.titleBold, FONTS.header3]}>Enter your Name, Email &</Text>
            <Text style={[styles.titleBold, FONTS.header3]}>Password to register</Text>
          </View>

          <View>
            <Text
              style={[{
                color: '#696969',
                marginTop: 32,
              }, FONTS.smallTitle]}>
              Full Name{' '}
            </Text>

            <View style={styles.inputContainer}>
              <TextInput
                style={[styles.input2, FONTS.body]}
                onChangeText={(text) => setName(text)}
                value={name}
                placeholder="john demo"
                placeholderTextColor={COLORS.placeHolderColor}
              />
            </View>
          </View>
          <Text
            style={[{
              color: '#696969',
              marginTop: 32,
            }, FONTS.smallTitle]}>
            Email address{' '}
          </Text>
          <View style={styles.inputContainer}>
            <TextInput
              style={[styles.input3, FONTS.body, { borderBottomColor: isEmailUnfocus ? '#C6C6C6' : isAvailable ? COLORS.primary : COLORS.red }]}
              onChangeText={(text)=> setValue(text)}
              onFocus={() => {
                setIsEmailUnfocus(false);
              }}
              onBlur={() => {
                setIsEmailUnfocus(true);
              }}
              // value={value}
              placeholder="abc@abc.com"
              placeholderTextColor={COLORS.placeHolderColor}
            />
          </View>
          {/* <Text style={{ color: color == 'red' ? COLORS.red : COLORS.primary, fontSize: 12 }}>{sms}</Text> */}

          <View>
            <Text
              style={[{
                color: '#696969',
                marginTop: 32,
              }, FONTS.smallTitle]}>
              Password
            </Text>

            <View style={styles.passwordContainer}>
              <TextInput
                style={[FONTS.body, { flex: 1, color: COLORS.black }]}
                onChangeText={(text) => setPin(text)}
                value={pin}
                secureTextEntry={secureEntry}
                placeholder="*****"
                placeholderTextColor={COLORS.placeHolderColor}
              />
              <TouchableOpacity
                onPress={() => {
                  setSecureEntry(!secureEntry)
                }}
              >
                <Image
                  source={secureEntry ? require('../../assets/images/input/EyeClose.png') : require('../../assets/images/input/EyeOpen.png')} //Change your icon image here
                  style={styles.ImageStyle}
                />
              </TouchableOpacity>
            </View>
          </View>

          <View
            style={{
              width: '100%',
              marginTop: 20,
              alignContent: 'center',
              justifyContent: 'center',
              alignItems: 'center',
              // backgroundColor: 'blue'
              opacity: value == ""  || name == "" || (pin == "" || pin.length < 5) ? 0.4 : 1
            }}>
            <ButtonArrow
              buttonText="Continue"
              disabled={value == ""  || name == "" || (pin == "" || pin.length < 5)}
              customStyle={{
                width: '100%',
                height: 53,
              }}
              onClick={() => checkEmail()}
              loading={isLoading}
            />
          </View>

          <View
            style={{
              marginTop: 16,
              alignItems: 'center',
            }}>

            <TouchableOpacity
              onPress={() => {
                navigation.navigate('loginOrReg')
              }}
              style={{
                marginTop: 15
              }}>
              <Text style={{
                color: COLORS.black, ...FONTS.body, borderWidth: 1,
                borderRadius: 9,
                borderColor: COLORS.gray10,
                paddingVertical: 12,
                paddingHorizontal: 20,
              }}>
                Or register with <Text style={{ color: COLORS.blackSolid, textDecorationLine: 'underline' }}>Phone number</Text>
              </Text>
            </TouchableOpacity>
          </View>

          {/* <View
            style={{
              marginTop: 7,
              alignItems: 'center',
              flexDirection: 'row',
              justifyContent: 'center',
            }}>
            <View style={styles.iconContainer}>
              <TouchableOpacity onPress={() => {
                navigation.navigate('loginOrReg')
              }} style={[styles.buttonBrand]}>
                <Image
                  style={{
                    resizeMode: 'contain',
                  }}
                  source={require('../../assets/images/input/Phone.png')}
                />
              </TouchableOpacity>
              <Text
                style={[FONTS.loginIcon, {
                  color: '#686868',
                }]}>
                Phone
              </Text>
            </View>
            <View style={styles.iconContainer}>

              <TouchableOpacity style={[styles.buttonBrand]}>
                <Image
                  style={{
                    resizeMode: 'contain',
                  }}
                  source={require('../../assets/images/input/Google.png')}
                />
              </TouchableOpacity>
              <Text
                style={[FONTS.loginIcon, {
                  color: '#686868',
                }]}>
                Google
              </Text>
            </View>
            <View style={styles.iconContainer}>

              <TouchableOpacity style={styles.buttonBrand}>
                <Image
                  style={{
                    resizeMode: 'contain',
                  }}
                  source={require('../../assets/images/input/Facebook.png')}
                />
              </TouchableOpacity>
              <Text
                style={[FONTS.loginIcon, {
                  color: '#686868',
                }]}>
                Facebook
              </Text>
            </View>

          </View> */}
        </ScrollView>
      </ContainerBackgroundImage>
    </View>
  );
};

export default RegistrationWithEmail;

const styles = StyleSheet.create({
  container: {
    flex: 1,
    paddingTop: 10,
    backgroundColor: 'white',
  },
  iconContainer: { flexDirection: 'column', justifyContent: 'center', alignItems: 'center', margin: 10 },
  contentText: {
    marginTop: 75,
  },
  titleNormal: {
    fontSize: 20,
    color: '#444444',
  },
  titleBold: {
    fontSize: 20,
    fontWeight: 'bold',
    color: '#444444',
  },
  inputContainer: {
    flexDirection: 'row',
    marginTop: 12,
  },
  input2: {
    width: '100%',
    height: 50,
    padding: 10,
    borderBottomWidth: 2,
    borderBottomColor: "#C6C6C6",
    color: COLORS.black
  },
  input3: {
    width: '100%',
    height: 50,
    padding: 10,
    borderBottomWidth: 2,
    color: COLORS.black
  },
  buttonBrand: {
    width: 52,
    height: 52,
    backgroundColor: '#FFFFFF',
    // flexDirection: 'row',
    justifyContent: 'center',
    alignItems: 'center',
    alignContent: 'center',
    borderRadius: 31,
    borderWidth: 2,
    borderColor: '#F5F5F5',
  },
  footer: {
    flex: 1,
    marginTop: 50,
    flexDirection: 'row',
    justifyContent: 'center',
    alignItems: 'center',
    alignContent: 'center',
  },
  textFooter: {
    fontSize: 15,
    color: '#696969',
    textAlign: 'center',
  },
  passwordContainer: {
    flexDirection: 'row',
    borderBottomWidth: 2,
    borderColor: '#C6C6C6',
    // paddingBottom: 10,
  },
  ImageStyle: {
    // padding: 10,
    // margin: 5,
    height: 32,
    width: 32,
    resizeMode: 'contain',
    alignItems: 'center',
  }
});
