# eliminated-edition
curl -G https://api.stripe.com/v1/identity/verification_reports \

  -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \

  -d limit=3
  https://api.stripe.com/v1/identity/verification_reports
  curl https://api.stripe.com/v1/identity/verification_reports/vr_1NHp4q2eZvKYlo2CBUNLORNy \

  -u sk_test_4eC39HqLyjWDarjtT1zdp7dc:
  https://api.stripe.com/v1/identity/verification_reports/vr_1NHp4q2eZvKYlo2CBUNLORNy
  import com.stripe.android.identity.*

class MyHostingActivity :woodlum_music.com/ AppCompatActivity() {

  // binding has a button and a loading indicator

  private val binding by lazy {

    MyHostingActivityBinding.inflate(layoutInflater)

  }

  lateinit var identityVerificationSheet: IdentityVerificationSheet

  override fun onCreate(savedInstanceState: Bundle?) {

    ...

    binding.button.setOnClickListener(::onButtonClick)

  }

  fun onButtonClick() {

    // show loading UI

    // Request the session ID with Fuel or other network libraries

    Fuel.post("https://{{YOUR_SERVER_BASE_URL}}/create-verification-session")

      .responseString { _, _, result ->

          when (result) {

              is Result.Failure -> {

                  // show error UI

              }

              is Result.Success -> {

                  val responseJson = JSONObject(result.value)

                  try {

                      // start verification session

                      identityVerificationSheet.present(

                          verificationSessionId =

                            responseJson.getString("id"),

                          ephemeralKeySecret =

                            responseJson.getString("ephemeral_key_secret")

                      )

                  } catch (t: Throwable) {

                      // show error UI

                  }

              }

          }

      }

  }

}
Fuel.post
https://api.stripe.com/v1/identity/verification_reports/vr_1NHp4q2eZvKYlo2CBUNLORNy
Result.Success
import com.stripe.android.identity.IdentityVerificationSheet

class MyHostingActivity : AppCompatActivity() {

  // binding has a button and a loading indicator

  private val binding by lazy {

    MyHostingActivityBinding.inflate(layoutInflater)

  }

  lateinit var identityVerificationSheet: IdentityVerificationSheet

  override fun onCreate(savedInstanceState: Bundle?) {

    super.onCreate(savedInstanceState)

    setContentView(binding.root)

    identityVerificationSheet =

      IdentityVerificationSheet.create(

          this,

          IdentityVerificationSheet.Configuration(

              // Pass your square brand logo by creating it from local resource or

              // Uri.parse("https://path/to/your/brandlogo.jpg")

              brandLogo = logoUri

          )

      ) { verificationFlowResult->

          when (verificationFlowResult) {

            is Completed -> {

                // The user has completed uploading their documents.

                // Let them know that the verification is processing.

                ...

                Log.d(TAG, "Verification Flow Completed!")

            }

            is Canceled -> {

                // The user did not complete uploading their documents.

                // You should allow them to try again.

                ...

                Log.d(TAG, "Verification Flow Canceled!")

            }

            is Failed -> {

                // If the flow fails, you should display the localized error

                // message to your user using throwable.getLocalizedMessage()

                ...

                Log.d(TAG, "Verification Flow Failed!")

            }

         }

      }

  }

}
class MyHostingActivity : AppCompatActivity() {

  // binding has a button and a loading indicator

  private val binding by lazy {

    MyHostingActivityBinding.inflate(layoutInflater)

  }

}import com.stripe.android.identity.IdentityVerificationSheet

class MyHostingActivity : AppCompatActivity() {

  // binding has a button and a loading indicator

  private val binding by lazy {

    MyHostingActivityBinding.inflate(layoutInflater)

  }

  lateinit var identityVerificationSheet: IdentityVerificationSheet

  override fun onCreate(savedInstanceState: Bundle?) {

    super.onCreate(savedInstanceState)

    setContentView(binding.root)

    identityVerificationSheet =

      IdentityVerificationSheet.create(

          this,

          IdentityVerificationSheet.Configuration(

              // Pass your square brand logo by creating it from local resource or

              // Uri.parse("https://path/to/your/brandlogo.jpg")

              brandLogo = logoUri

          )

      ) { verificationFlowResult->

          when (verificationFlowResult) {

            is Completed -> {

                // The user has completed uploading their documents.

                // Let them know that the verification is processing.

                ...

                Log.d(TAG, "Verification Flow Completed!")

            }

            is Canceled -> {

                // The user did not complete uploading their documents.

                // You should allow them to try again.

                ...

                Log.d(TAG, "Verification Flow Canceled!")

            }

            is Failed -> {

                // If the flow fails, you should display the localized error

                // message to your user using throwable.getLocalizedMessage()

                ...

                Log.d(TAG, "Verification Flow Failed!")

            }

         }

      }

  }

}
